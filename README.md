# &lt;time&gt; element extensions

Formats date as a localized string or as relative text that auto updates in the user's browser.

## Installation

Available on [Bower](http://bower.io) as **time-elements**.

```
$ bower install time-elements
```

This component is built on the upcoming [Web Component](http://webcomponents.github.io/) stack. Specifically, it requires a feature called [Custom Elements](http://www.html5rocks.com/en/tutorials/webcomponents/customelements/). You'll need need to use a Polyfill to get this feature today. Either the [Polymer](http://www.polymer-project.org/) or [X-Tag](http://www.x-tags.org/) frameworks supply a polyfill or you can install the standalone [CustomElements](https://github.com/Polymer/CustomElements) polyfill.

``` html
<script src="https://cdnjs.cloudflare.com/ajax/libs/polymer/0.2.2/platform.js"></script>
```


## Usage

All elements MUST have a `datetime` attribute set to a ISO 8601 formatted timestamp.

``` html
<time is="local-time" datetime="2014-04-01T16:30:00-08:00" month="short" day="numeric" year="numeric" hour="numeric" minute="numeric">
  04/01/14 4:30PM PDT
</time>
<!-- <time is="local-time" title="Apr 1, 2014 6:30PM PDT">Apr 1, 2014 6:30PM</time> -->
```

A relative time-ago-in-words description can be generated by using the `relative-time` element extension.

``` html
<time is="relative-time" datetime="2014-04-01T16:30:00-08:00">
  04/01/14
</time>
<!-- <time is="relative-time">1 week ago</time> -->
```

An *always* relative time-ago-in-words description can be generated by using the `time-ago` element extension.

``` html
<time is="time-ago" datetime="2012-04-01T16:30:00-08:00">
  04/01/12
</time>
<!-- <time is="time-ago">2 years ago</time> -->
```


### Options

Attribute      | Options                        | Description
---            | ---                            | ---
`datetime`     | ISO 8601 date                  | Required date of element `2014-06-01T13:05:07Z`
`year`         | 2-digit, numeric               | Format year as `14` or `2014`
`month`        | short, long                    | Format month as `Jun` or `June`
`day`          | 2-digit, numeric               | Format day as `01` or `1`
`weekday`      | short, long                    | Format weekday as `Sun` or `Sunday`
`hour`         | 2-digit, numeric               | Format hour as `01` or `1`
`minute`       | 2-digit, numeric               | Format minute as `05` or `5`
`second`       | 2-digit, numeric               | Format second as `07` or `7`

## Browser Support

![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
Latest ✔ | Latest ✔ | 9+ ✔ | Latest ✔ | 6.1+ ✔ |


## See Also

Most of this implementation is based on Basecamp's [local_time](https://github.com/basecamp/local_time) component. Thanks to @javan for open sourcing that work and allowing for others to build on top of it.

@rmm5t's [jquery-timeago](https://github.com/rmm5t/jquery-timeago) is one of the old time-ago-in-words JS plugins.
