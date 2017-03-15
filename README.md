# video-wrapper
Responsive video container for embed/object/iframe videos. This uses the bourbon mixins <a href="http://bourbon.io/docs/#position" target="_blank">position</a> & <a href="http://bourbon.io/docs/#size" target="_blank">size</a>.

```html
.video-wrapper {
  height: 0;
  overflow: hidden;
  padding-bottom: 56.25%; // 16:9
  //padding-bottom: 75%; // 4:3
  position: relative;

  embed,
  object,
  iframe {
    @include position(absolute, 0 null null 0);
    @include size(100%);
  }
}
```

Example Usage:
```html
<div class="video-wrapper">
  <iframe src="https://player.vimeo.com/video/87110435?title=0&byline=0&portrait=0" width="640" height="360" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
</div>
```
