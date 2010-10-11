## achtung for jQuery ##

This is a simple notifications plugin for jQuery.  Check out the [demo page](http://voxwerk.github.com/jquery-achtung/src/demo.html).

### Examples ###

A sticky notification:

    var notice = $.achtung({
        timeout: 0,
        className: 'achtungSuccess',
        icon: 'ui-icon-check',
        message: 'This is a sticky notification!'
    });

    // To close
    notice.achtung('close');

The following notification closes automatically after 5 seconds:

    var notice = $.achtung({
        timeout: 5, // Seconds
        className: 'achtungSuccess',
        icon: 'ui-icon-check',
        message: 'This is a timed notification!'
    });

    // If you get tired of waiting, you can still close it
    notice.achtung('close');

Loading message that turns into a timed success notice:

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
