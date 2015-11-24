
ResponsiveMultiLevelMenu
=========

This is a forked version of this library.

I changed it to allow for an alternate $trigger (jQuery collection).

I also added onNavOpened() and onNavClosed() callbacks to allow for running code after these events occur.

index2.html contains this new use case:

    <script>
        $(function() {
            var $trigger = $(".alt.dl-trigger");
            $( '#dl-menu' ).dlmenu({
                animationClasses : { classin : 'dl-animate-in-2', classout : 'dl-animate-out-2' },
                triggerEl: $trigger,
                onNavOpened: function(){
                    $(".status").text("nav-open");
                },
                onNavClosed: function(){
                    $(".status").text("nav-closed");
                }
            });
        });
    </script>


Orig README:: 
========

A responsive multi-level menu that shows its submenus in their own context, allowing for a space-saving presentation and usage.

[article on Codrops](http://tympanus.net/codrops/?p=14753)

[demo](http://tympanus.net/Development/ResponsiveMultiLevelMenu)

Licensed under the MIT License