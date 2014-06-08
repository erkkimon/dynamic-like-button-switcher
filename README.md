dynamic-like-button-switcher
============================

How to utilize the visitors will to like after he/she has already liked your FB page using the like button? If he has liked your FB page, he can still like the current URL. That's what this library does; shows the button to like your FB page, and after clicking that the visitor will see a button to like the current URL instead.

How to use?
===========

You probably understand this quite well if you just read the index.html, which is an example. The detailed instructions below might just confuse you, because this isn't really very complicated. Just add the libraries, add placeholder for the like button and call dynamicLikeButtonSwitcher with the information abuot your FB page address, and then lib/dynamic-like-button-switcher.js can do the magic.

The dynamic-like-button-switcher depends on jQuery and iFrameTracker. To use dynamic-like-button-switcher, you need to reference to jQuery, iFrameTracker and dynamic-like-button-switcher and then add proper placeholder in your source code to the position you want the like button ot appear. See the index.html, which is a minimal example.

First add the following lines in the head of your HTML document.
```html
<script src="http://code.jquery.com/jquery-1.9.0.min.js"></script>
<script src="lib/jquery.iframetracker-1.3.js"></script>
<script src="lib/dynamic-like-button-switcher.js"></script>
```
In the code above I link to jQuery not hosted by me, but of course it can be hosted by you also. You also need iFrameTracker to detect clicks on Facebook Like Button. I used the version 1.3 and iFrameTracker can be downloaded on Github (https://github.com/finalclap/iframeTracker-jquery), named it as jquery.iframetracker-1.3.js and put it in "lib" subdirectory. I also sourced the dynamic-like-button-switcher.js in "lib", which is the magical and essential part in this repository.

After linking the necessary libraries to your index.html, placeholder needs to be added. The class name of the div containing the iframe needs to be "likebutton-placeholder".
```html
<div class="likebutton-placeholder">
  <iframe></iframe>
</div> 
```
And finally, you will need to call dynamicLikeButtonSwitcher() defined in dynamic-like-button-switcher.js library with the link to your FB page address as a parameter. dynamicLikeButtonSwitcher() should be called from $(document).ready(), e.g. like this.
```javascript
<script>
  $(document).ready(function() 
  {
    dynamicLikeButtonSwitcher("https://www.facebook.com/personaltravis");
  }); 
</script>
```
