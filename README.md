**Custom Youtube player**

With show/hide youtube functions and POSTER DIV


This allows you to create a div with images and overlay divs to make up an awesome video card.


+ Includes Play button function, shows div containing Youtube iframe.
+ Starts playing with sound ON. (auto unmutes when default is set to mute)
+ Hides youtube div when youtube video is paused.


When you code your videocard html file just create a play button that calls the function.
```
use: onclick="showVideo()"
```

Also create a div wrap for the Youtube iframe with an ID value of "youtube"

example:
```
<div class="youtube">
    <iframe 
    id="video" 
    src="https://www.youtube.com/embed/FQmmD5PEd4U?enablejsapi=1" 
    frameborder="0"
    allow="autoplay" 
    allowfullscreen></iframe>
</div>
```

Make sure ```?enablejsapi=1``` is in the youtube embed link.
