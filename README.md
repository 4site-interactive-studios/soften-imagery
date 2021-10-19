# Soften Imagery

Some projects require you to work with graphic imagery, but that doesn't mean you want to stare at it all day. The following CSS styles will try and blur, grayscale, and reduce opacity on all graphic images and video, with the option for a four second hover state to reveal the underlying media.

Simply copy the the code below and paste into this website https://mcdlr.com/css-inject/

Then drag and drop the bookmarklet into your browser: https://d.pr/v/6sxmnm

Now when you visit a page, click the bookmarklet to inject the styles into your page. https://d.pr/v/PLeEFA

    img,
    picture,
    video,
    [src*='youtube' i],
    [src*='vimeo' i],
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
    html [style*='background-image' i]:hover,
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
    
## Todo
* wrap it all in JS that adds an explicit class to img, picture, video, iframe with video elements. This way you have CSS catch alls for background media and explicit classes for inline media.
* Add a bookmarklet that people can drag/drop directly from here
