flot.stackpercent
=================

This is a plugin for jQuery flot, to create chart as stacked percentage.

This plugin is based on another plugin `jQuery.flot.stack.js` which can be found on <http://code.google.com/p/flot/>

Option to enable stackpercent:

```
series: {stackpercent: true}
```

You may need to set options `yaxis:{max:100}` to make the yaxis is 0-100.

It can work with another plugin called `flot.tooltip` <https://github.com/skeleton9/flot.tooltip> to easily show y value, percentage and x value.

