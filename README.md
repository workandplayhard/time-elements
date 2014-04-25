# &lt;local-time&gt; Element

Formats date as a localized string or as relative text that auto updates in the user's browser.

## Installation

Available on [Bower](http://bower.io) as **local-time-element**.

```
$ bower install local-time-element
```

Installing from Bower will also the [Moment.js](http://momentjs.com/) dependency.

This component is built on the upcoming [Web Component](http://webcomponents.github.io/) stack. Specifically, it requires a feature called [Custom Elements](http://www.html5rocks.com/en/tutorials/webcomponents/customelements/). You'll need need to use a Polyfill to get this feature today. Either the [Polymer](http://www.polymer-project.org/) or [X-Tag](http://www.x-tags.org/) frameworks supply a polyfill or you can install the standalone [CustomElements](https://github.com/Polymer/CustomElements) polyfill.

``` html
<script src="https://cdnjs.cloudflare.com/ajax/libs/polymer/0.2.2/platform.js"></script>
```


## Usage

``` html
<local-time datetime="2014-04-01T16:30:00-08:00" format="%m/%d/%y %l:%M%p">
  04/01/14 4:30PM PDT
</local-time>
<!-- <local-time>04/01/14 6:30PM</local-time> -->
```

All elements MUST have a `datetime` attribute set to a ISO8601 formatted timestamp. `format` is a unix strftime format to set to the text contents of the element.

``` html
<local-time datetime="2014-04-01T16:30:00-08:00" format="%m/%d/%y" title-format="%m/%d/%y %l:%M%p">
  04/01/14
</local-time>
<!-- <local-time title="04/01/14 6:30PM">04/01/14</local-time> -->
```

A title attribute has also be given a local format by setting `title-format`.

A relative time ago in words description can be generated by setting a `from` range. The value can either be a static ISO8601 string or the string `"now"` which automatically computes from the current time.

``` html
<local-time datetime="2014-04-01T16:30:00-08:00" from="now">
  04/01/14
</local-time>
<!-- <local-time>1 week ago</local-time> -->
```

## Browser Support

Chrome (latest), Safari (6.1+), Firefox (latest) and IE 9+.

## See Also

Most of this implementation is based on Basecamp's [local_time](https://github.com/basecamp/local_time) component. Thanks to @javan for open sourcing that work and allowing for others to build on top of it.

[Moment.js](http://momentjs.com/) is a popular date parsing and timeago JS library.

@rmm5t's (jquery-timeago)[https://github.com/rmm5t/jquery-timeago] is one of the olds timeago in words JS plugins.
