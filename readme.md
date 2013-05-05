# Glisse.js

Glisse.js is a simple, responsive and fully customizable jQuery photo viewer.
You'll like the transitions between two photos entirely assumed by CSS3.

To see the plugin in action here is two examples with some lovely photos of my friend [Pierre Nizet](http://www.pierre-nizet.fr/).

Feel free to fork the project on github or ping me on [twitter](http://twitter.com/_victa) for any comments.

<a href='http://www.pledgie.com/campaigns/17334'><img alt='Click here to lend your support to: Glisse.js and make a donation at www.pledgie.com !' src='http://www.pledgie.com/campaigns/17334.png?skin_name=chrome' border='0' /></a>

#### Demonstrations

* [Example #1](http://glisse.victorcoulon.fr/example-1)
* [Example #2](http://glisse.victorcoulon.fr/example-2)

#### Features

* Keyboard navigation
* Fully CSS Customizable
* Animated with CSS3 keyframes
* 7 different transition effects
* Scale to the viewport
* Fullscreen support
* iPad & iPhone ready _(soon a fully Android support)_

#### Warning
This plugin uses a lot of new CSS3 features like keyframes. It’s definitely not a good idea to uses it on a general public website for the time. But my goal -if the plugin has good returns- is to make a fully compliant plugin, using javascript animation on old browsers. So stay tuned.

#### Roadmap

* Fallbacks for old browsers
* Add a paging
* Add an autoplay feature

## Documentation

### Basic Usage

Put this script just after jquery in your document

    <script src="glisse.js"></script>

Then include the base stylesheet (**Before you own stylesheets**)

This stylesheet contains the base style for Glisse.js but there are not visual style included!!

    <link rel="stylesheet" href="glisse.css" />

Add a "data-glisse-big" attribute to your image. This attribute corresponds to your full view picture.

    <img class="pics" src="thumb.jpg" data-glisse-big="big.jpg"/>

If you want image shows/groups, simply add a "rel" attribute to your links

    <img class="pics" src="thumb-1.jpg" data-glisse-big="big-1.jpg" rel="group1"/>
    <img class="pics" src="thumb-2.jpg" data-glisse-big="big-2.jpg" rel="group1"/>
    <img class="pics" src="thumb-3.jpg" data-glisse-big="big-3.jpg" rel="group1"/>

If you want show a title during the slideshow, simply use the "title" attribute

    <img class="pics" src="thumb-1.jpg" data-glisse-big="big-1.jpg" rel="group1" title="my awesome picture"/>
    <img class="pics" src="thumb-2.jpg" data-glisse-big="big-2.jpg" rel="group1" title="wooh, another picture"/>

After it, call the plugin.

    <script>
        $(function () {
            $('.pics').glisse({
                changeSpeed: 550, 
                speed: 500,
                effect:'bounce',
                fullscreen: true
            }); 
        });
    </script>

### Options

Valid options for glisse.js are:

* ``changeSpeed`` - Transition duration between 2 pictures (default ``1000``)
* ``speed`` - Open/Close slideshow duration (default ``300``)
* ``dataName`` - change the data attribute name for fullscreen pictures (default ``data-glisse-big``)
* ``fullscreen`` - fullscreen gallery using fullscreen api (default ``false``)
* ``disablindRightClick`` - disabling right click on full size picture (default ``false``)
* ``effect`` - Effect (default ``bounce``)
    * __Valid effect values:__
    * bounce
    * fadeBig
    * fade
    * roll
    * rotate
    * flipX
    * flipY

                       
##Compatibility

* Firefox 4+
* Opera 11.6+
* Chrome 14+
* Safari 5+
* iPhone/iPad iOS 4.3+
* BlackBerry OS v6+

Works but without CSS3 transitions:

* Opera 10+
* Firefox 3.6
* IE8+
 
## Credits

* Author: [Victor Coulon](http://victorcoulon.fr) or ping me on [twitter](http://twitter.com/_victa)
* Photos by [Pierre Nizet](http://www.pierre-nizet.fr/)
* Inspiration for CSS3 animations : [Animate.css](http://daneden.me/animate/)


## Licence

Licence Mit