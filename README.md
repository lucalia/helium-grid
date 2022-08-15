# Helium Grid

A lightweight alternative for the BootStrap grid functionality.

## Mission

To provide basic grid functionality with the fewest bytes possible.

Helium Grid is designed to be super easy to implement in any project, requiring minimal modification to existing code. However, the primary goal is to provide this functionality with the smallest file that can possibly be sent across the wire.

```
https://cdn.jsdelivr.net/gh/lucalia/helium-grid@0.9.1/helium-grid.min.css
```

## Getting Started

There are two ways that Helium Grid can be used...

### The Easy Way

The simplest way to use this framework is to call our CDN. We would strongly encourage you, however, to use The Hard Way. It's much more performant (and the whole point of Helium Grid is to increase performance).

### The Hard Way

To start out with, your project should definitely already be using a preprocessor. We use SASS (if you use LESS or another, it should be easy enough to convert). Simply pull `_grid.scss` into your local project, and import the partial into your main SASS file

```
    @import 'grid';
```

I guess that really wasn't that much harder... makes you wonder why people don't do it this way to begin with.

## How To Use

Helium Grid is very simple by design. All you need to get started is a parent container with the class `helium-grid`. Within that parent, you can pretty much use the default BootStrap 4.x column naming conventions.

```
    <div class="helium-grid">
        <div class="sm-3></div>
        <div class="sm-6></div>
        <div class="sm-3></div>
    </div>
```

If you don't fill an entire row, the elements you do provide are centered by default.

```
    <!-- Only 6 of the 12 available columns are used -->
    <div class="helium-grid">
        <div class="sm-3></div>
        <div class="sm-3></div>
    </div>
```

Should you desire different layouts across different device types, you can add a class for each screen size. If you do not specify a width for xs screen sizes, the default is to take an entire row.

```
    <!-- All rows will take 100% width on mobile devices, since xs sizing is not specified -->
    <div class="helium-grid">
        <div class="sm-6 md-4 lg-3 xl-2></div>
        <div class="sm-6 md-4 lg-3 xl-2></div>
        <div class="sm-6 md-4 lg-3 xl-2></div>
        <div class="sm-6 md-4 lg-3 xl-2></div>
        <div class="sm-6 md-4 lg-3 xl-2></div>
        <div class="sm-6 md-4 lg-3 xl-2></div>
    </div>
```

Parent containers can be nested as many times as you deem fit in order to get the layout you desire. 

```
    <div class="helium-grid">
        <div class="helium-grid sm-6 md-4 lg-3 xl-2>
            <div class="xs-4"></div>
            <div class="xs-4"></div>
            <div class="xs-4"></div>
        </div>
        <div class="sm-6 md-4 lg-3 xl-2></div>
        <div class="sm-6 md-4 lg-3 xl-2></div>
        <div class="sm-6 md-4 lg-3 xl-2></div>
        <div class="sm-6 md-4 lg-3 xl-2></div>
        <div class="sm-6 md-4 lg-3 xl-2></div>
    </div>
```

## Customization

If using [The Hard Way](#the-hard-way), you can modify the source code however you please and recompile. If you discover an amazing way to improve Helium Grid, please submit a pull request, I'd love to see this improve!

If you decide our device sizes don't fit your needs, there is a `Variables` section in the source code where all these values are defined anc can be modified.
