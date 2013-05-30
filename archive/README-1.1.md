jQuery-Open
===========

## New in 1.1 ##
    - Now only works by event delegation.
    - Add event on load, on view for ajax and iframe mode.
    - Enable to close iframe or ajax box by clicking outside it.
    - Add closure tag on top of iframe or ajax box.
    - Manage maximum number of tab also from ajax box.
    - Convert # as ? in url for ajax mode

=======

Enable various methods to open links:
    - In iframe
    - In popup
    - In current window of course
    - With Ajax call

Can manage all HTML tags with jQuery data "url", data "erl" (link encoded with rot13 method) or basically with "a" tag.

You can complete current url dynamically with data "arg" and with an unique identifier named "i", generated by this plugin.

Various options, like autoading of the first element are available, or the toggle display on click for one element loaded, etc.
See settings for more informations.


## Examples ##

You can also specify 3 type of opening. By default "self", open it in current view, "popup" in new window and "iframe" enable to show url in iframe with loading message:

    $.open("span.a");

And, you can specify various properties to extend common behaviors, here for example we open the first element on load: 

    $.open("span.a", {type: 'iframe', autoload: true});

Attach events when the element exits of the current view. The DOM element has been passed as first parameter:

    $.open("a, span.a", {
        onExit : function (elem){ console.log('Bye'); },
    });

And if you want to change the container of the delegation, this one :

    $.open('.a, span.a', {container: '.myContainer'});

You can use data "erl" to store URL encoded with Rot13 transformation. Perform to obfuscate some links.

Finally you can overload common behavior of a list by adding classname on each element (self, blank or iframe).