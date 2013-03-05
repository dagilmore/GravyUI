SimpleUI
========

A starting-point UI framework for quick development.  This framework isn't meant to be an "end-all" or a "go-to" framework to replace popular UI frameworks like jQueryUI, Foundation, KendoUI, or Twitter Bootstrap.  Rather, this framework is meant to give anyone a "barebones" starting point with which to build their own UI.  I've done as much of the heavy-lifting as I see fit to comprise a basic framework.  The rest is on you to really tailor the product to your own needs.  Clone, edit, enjoy friends!

Documentation
========

Currently the following UI elements are supported:
* Text input (`<input>`)
  * Text
  * Email
  * Hidden (by nature)
  * Search
  * Password
  * Email
  * File (see below for documentation)
* Textarea (`<textarea>`)
* Radio (`<input type="radio">`)
* Checkbox (`<input type="checkbox">`)
* Submit (`<input type="submit">`)
* Progress Bar (see below for documentation)
* Meter (see below for documentation)
  * Vertical
  * Horizontal
* Slider (see below for documentation)
  * Vertical
  * Horizontal
* Dialog Window (see below for documentation)
* Table (`<table>`)
* Accordion (see below for documentation)
* All form-based elements (`<form>`, `<legend>`, `<fieldset>`)



###File Input
========
```
<div class="file">
    <input type="file">
    <input type="text" placeholder="Upload file...">
</div>
```

The reason for this is that `<input type="file">` isn't really possible to style without hacking around a bit.  For more information, please read up at [QuirksMode](http://www.quirksmode.org/dom/inputfile.html).

###Progress Bar
========
```
<!-- Span tag descriptions are optional, but look pretty cool... -->
<div class="progressBar">
    <div class="progress" style="width: 68%;">
        <span class="desc1">this is <b>68%</b></span>
    </div>
    <div class="remainder" style="width: 32%;">
        <span class="desc2"> of the total</span>
    </div>
</div>
```

The browser support for the `<progress>` tag right now (March 5th, 2013) is rather unacceptable for mobile browsers and pretty recent of an addition to modern browsers (with scanty IE support).  In my opinion, it's simply not worth it at the moment to use the HTML5 tag, not to mention the incredibly limited amount of styling available.  [Look here](http://caniuse.com/progressmeter) for more information on browser support.

###Meter
========
```
<div class="meter">
    <div class="progress" style="width: 68%;"></div>
    <div class="remainder" style="width: 32%;"></div>
</div>
<!-- This one is vertical! -->
<div class="meter vertical">
    <div class="remainder" style="height: 32%;"></div>
    <div class="progress" style="height: 68%;"></div>
</div>
```

My explanation for the Progress Bar section is the same for the Meter section.

###Slider
========
```
<div class="range">
    <div class="bar"></div>
    <div class="slide" style="left: 38%;"></div>
</div>
<!-- This one is vertical! -->
<div class="range vertical">
  	<div class="bar"></div>
    <div class="slide" style="bottom: 38%;"></div>
</div>
```

Don't let the names "range" and "slider" confuse you.  The reasoning is because of HTML5's new `<input>` type "range", which at this point (March 5th, 2013) has absolutely no support for Firefox or Opera Mini ([source](http://caniuse.com/#feat=input-range)).  Until I see that support, I'm going to go with some simple HTML4 and Javascript.

###Dialog Window
========

```
<div class="window movable">
    <div class="titleBar">
        <h3>Title of the window</h3>
        <span class="close">x</span>
    </div>
    <div class="windowContent">
      	<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque quam purus, faucibus a rhoncus a, pretium eu lacus. Vestibulum ligula nunc, gravida nec consequat vel, tempus at lorem. Donec in quam nec dui pellentesque mattis. Donec feugiat odio eu leo feugiat lacinia. Sed a arcu tortor. Curabitur in est odio, sit amet sodales mauris. Suspendisse potenti. Cras ullamcorper dapibus dictum. Nulla vitae eros urna, sed pretium dolor. Integer id ultrices nulla. Praesent ut orci nunc. Quisque diam arcu, gravida vel molestie vitae, convallis a ipsum. Proin tristique leo nisi. Morbi pretium lacinia est eu suscipit. Curabitur et nisi in enim convallis adipiscing. Curabitur bibendum rhoncus lacus, vel imperdiet velit convallis sed.</p>
    </div>
    <div class="buttons">
        <button>OK</button>
    </div>
</div>
```

This should be pretty self-explanatory.  If not, you can attach a movable class (like in the example above) to be able to drag the dialog window wherever you'd like on the screen, otherwise it defaults to it's position.  The window content can be anything you can imagine and there's room for a title and close button up top as well as a slew of buttons down below.

###Accordion
========

```
<div class="accordion">
    <div class="header">
        <ul class="notList">
            <li>Field 1</li>
            <li>Field 2</li>
        </ul>
    </div>
    <div class="itemHead">
        <ul class="notList">
          	<li><span class="rightArrow"></span>Value 1</li>
            <li>Value 1 Description</li>
        </ul>
    </div>
    <div class="itemFold">
        <ul class="notList">
            <li>Fold 1</li>
            <li>Fold 1 Description</li>
        </ul>
    </div>
</div>
```

The accordion is designed to hide and show information upon click.  It looks pretty identical to the `<table>`, but allows for content to drop in underneath it.  Fancy.


Support
========
If there's any questions, comments, or thoughts about the SimpleUI then let me know at [my email](mailto:me@patrickcason.com).  I'll do my best to get back to you as soon as possible.  If you think you can make the project better, then clone the repo and play with it.  I'd love to see what you come up with!