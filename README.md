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

Example:
```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
<html>
 <head>
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
    <title>Flot Examples</title>
    <!--[if lte IE 8]><script language="javascript" type="text/javascript" src="../excanvas.min.js"></script><![endif]-->
    <script language="javascript" type="text/javascript" src="../jquery.js"></script>
    <script language="javascript" type="text/javascript" src="../jquery.flot.js"></script>
    <script language="javascript" type="text/javascript" src="../jquery.flot.stackpercent.js"></script>
 </head>
    <body>
    <h1>Flot Examples: Stackpercent</h1>

    <div id="placeholder" style="width:600px;height:300px;"></div>

<script id="source">
$(function () {

     var data = [
     {"label":"<50%","data":[[0, null], [1, 1]],"color":"#B41722"},
     {"label":">=50%","data":[[0, null],[1, null]],"color":"#E78800"},
     {"label":">=90%","data":[[0, 1],[1, null]],"color":"#83BA4F"},
     {"label":"Passed","data":[[0, 2], [1, 1]],"color":"#6A9A3C"} ];


    $.plot($("#placeholder"), data, {
        series: {
            stackpercent: true,
            bars: { show: true, barWidth: 0.6, fillColor: {colors:[{opacity: 1},{opacity: 1}]}, align: "center" }
        },
        xaxis: {tickSize : 1},
        yaxis:{max:100}
    });
});
</script>

 </body>
</html>
```