Some projects require you to work with graphic imagery, but that doesn't mean you want to stare at it all day. The following CSS styles will try and blur, grayscale, and reduce opacity on all graphic images and video, with the option for a four second hover state to reveal the underlying media.

<img src="https://raw.githubusercontent.com/4site-interactive-studios/soften-imagery/main/before-and-after-v2.jpg" style="max-width: 100%" alt="Screenshot of theatlantic.com homepage showing a before and after comparison of using the Soften Imagery bookmarklet">

## How to Use

1. Copy the the code below and paste into this website https://mcdlr.com/css-inject/
2. Then drag and drop the bookmarklet into your browser: https://d.pr/v/6sxmnm
3. Now when you visit a page, click the bookmarklet to inject the styles into your page. https://d.pr/v/PLeEFA

### Code to Copy

    img,
    picture,
    video,
    [src*='youtube' i],
    [src*='vimeo' i],
    [style*='background: url' i],
    [style*='background-image' i],
    [class~='background' i],
    [class~='backgroundimage' i],
    [class~='background-image' i],
    [class~='background_image' i],
    [class~='bgimage' i],
    [class~='bg-image' i],
    [class~='bg_image' i]{
        filter: blur(10px) grayscale(100%);
        opacity: 0.5;
        transition-duration: 0s;
        transition-timing-function: ease-in;
    }
    
    html img:hover,
    html picture:hover,
    html video:hover,
    html [src*='youtube' i]:hover,
    html [src*='vimeo' i]:hover,
    html [style*='background: url' i]:hover,
    html [style*='background-image' i]:hover,
    html [class~='background' i],
    html [class~='backgroundimage' i]:hover,
    html [class~='background-image' i]:hover,
    html [class~='background_image' i]:hover,
    html [class~='bgimage' i]:hover,
    html [class~='bg-image' i]:hover,
    html [class~='bg_image' i]:hover{
        filter: blur(0px) grayscale(0%);
        opacity: 1;
        transition-duration: 4s;
    }
