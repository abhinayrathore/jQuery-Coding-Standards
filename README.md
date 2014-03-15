jQuery Coding Standards and Best Practices
=======================

## Loading jQuery
1. Always try to use a CDN to include jQuery on your page. [CDN Benefits](http://www.sitepoint.com/7-reasons-to-use-a-cdn/)
  ```
  <script type="text/javascript" src="//ajax.googleapis.com/ajax/libs/jquery/1.11.0/jquery.min.js"></script>
      <script>window.jQuery || document.write('<script src="js/jquery-1.11.0.min.js" type="text/javascript"><\/script>')</script>
  ```
  Popular jQuery CDNs: [Google](https://developers.google.com/speed/libraries/devguide#jquery), [Microsoft](http://www.asp.net/ajaxlibrary/cdn.ashx#jQuery_Releases_on_the_CDN_0), [jQuery](http://jquery.com/download/), [cdnjs](http://cdnjs.com/libraries/jquery/), [OSSCdn](http://osscdn.com/#/jquery)

2. Implement a fallback to your locally hosted library of same version as shown above. [More Info](http://css-tricks.com/snippets/jquery/fallback-for-cdn-hosted-jquery/)

3. Use [protocol-relative/protocol-independent](http://www.paulirish.com/2010/the-protocol-relative-url/) URL (leave ```http:``` or ```https:``` out) as shown above.

4. If possible, keep all your JavaScript and jQuery includes at the bottom of your page. [More Info](http://developer.yahoo.com/blogs/ydn/high-performance-sites-rule-6-move-scripts-bottom-7200.html) and a sample on [HTML5 Boilerplate](https://github.com/h5bp/html5-boilerplate/blob/master/index.html).

5. What version to use?
  - DO NOT use jQuery version 2.x if you support Internet Explorer 6/7/8.
  - For new web-apps, if you do not have any plugin compatibility issue, it's highly recommended to use the latest jQuery version.
  - When loading jQuery from CDN's, always specify the complete version number you want to load (Example: _1.11.0_ as opposed to _1.11_ or just _1_).
  - DO NOT load multiple jQuery versions.

6. If you are using other libraries like Prototype, MooTools, Zepto etc. that uses ```$``` sign as well, try not to use ```$``` for calling jQuery functions and instead use jQuery simply. You can return control of ```$``` back to the other library with a call to ```$.noConflict()```.

7. For advanced browser feature detection, use [Modernizr](http://modernizr.com/).


