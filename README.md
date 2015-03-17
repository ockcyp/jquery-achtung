## achtung for jQuery ##

This is a simple notifications plugin for jQuery.  Check out the [demo page](http://voxwerk.github.com/jquery-achtung/src/demo.html).

### Examples ###

A sticky notification:

```js
var notice = $.achtung({
    timeout: 0,
    className: 'achtungSuccess',
    icon: 'ui-icon-check',
    message: 'This is a sticky notification!'
});

// To close
notice.achtung('close');
```

The following notification closes automatically after 5 seconds:

```js
var notice = $.achtung({
    timeout: 5, // Seconds
    className: 'achtungSuccess',
    icon: 'ui-icon-check',
    message: 'This is a timed notification!'
});

// If you get tired of waiting, you can still close it
notice.achtung('close');
```

Loading message that turns into a timed success notice:

```js
var notice = $.achtung({
    timeout: 0,
    className: 'achtungWait',
    icon: 'wait-icon',
    message: 'Loading..'
});

// Once you're ready to report that you're done:
notice.achtung('update', {
    timeout: 10,
    className: 'achtungSuccess',
    icon: 'ui-icon-check',
    message: 'Loading complete!'
});
```

Use jQuery to interact with the notifications:

```js
$.achtung({ timeout: 0, message: 'Notice #1' });
$.achtung({ timeout: 0, message: 'Notice #2' }).attr('id', 'notice2');
$.achtung({ timeout: 0, message: 'Notice #3' });

// Close the first notice
$('.achtung:first').achtung('close');
// Close by ID selector
$('#notice2).achtung('close');
```
