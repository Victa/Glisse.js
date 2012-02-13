# Glisse.js

Glisse.js is a simple, responsive and fully customizable jQuery photo viewer.
You'll like the transitions between two photos entirely assumed by CSS3.

To see the plugin in action here is two examples with some lovely photos of my friend [Pierre Nizet](http://www.pierre-nizet.fr/).

Feel free to fork the project on github or ping me on [twitter](http://twitter.com/_victa) for any comments.

#### Demonstrations

* [Example #1](http://glisse.victorcoulon.fr/example-1)
* [Example #2](http://glisse.victorcoulon.fr/example-2)

#### Features

* Keyboard navigation
* Fully CSS Customizable
* Animated with CSS3 keyframes
* 7 different transition effects
* Scale to the viewport
* iPad & iPhone ready _(soon a fully Android support)_

#### Warning
This plugin uses a lot of new CSS3 features. It's definitely not a good idea to uses this plugin on a general public website for the time.
But now my goal is to make a fully compliant plugin, using javascript on old browsers. So stay tuned.

## Documentation

### Basic Usage

Put this script just after jquery in your document

    <script src="glisse.js"></script>

Then include the base stylesheet (**Before you own stylesheets**)

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
                effect:'bounce'
            }); 
        });
    </script>

### Options

Valid options for glisse.js are:

* ``changeSpeed`` - Transition duration betwwen 2 pictures (default ``1000``)
* ``speed`` - Open/Close slideshow duration (default ``300``)
* ``dataName`` - change the data attribute name for fulscreen pictures (default ``data-glisse-big``)
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

Works but without CSS3 trantions:

* Opera 10+
* Firefox 3.6
* IE8+
 
## Credits

* Author: [Victor Coulon](http://victorcoulon.fr) or ping me on [twitter](http://twitter.com/_victa)
* Photos by [Pierre Nizet](http://www.pierre-nizet.fr/)
* Inspiration for CSS3 animations : [Animate.css](http://daneden.me/animate/)


## Licence

Licence Mit