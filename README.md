### Scroll on iOS 15 

Safari on IOS 15 has a new 'feature'. It hides address bar when you swipe down, and when you swipe up it shows it again.
In this repo you can find my dirty workaround, which is solving this issue.

[Go and test it!](https://andriibarvynko.github.io/ios15_scroll_test/src/index.html)

Personally I've tested this on iPhone 11 Pro and iPhone 8+, iOS 15.1

### How it works:

You need to use viewport meta and the following structure:

```html
<head>
    <meta name="viewport" content="width=device-width, height=device-height"/>
</head>
<body>
    <div class="outer-content">
        <div id="content">
            <!-- Scrollable content here -->
        </div>
    </div>
</body>
```

And the following css for the outer container:

```css
.outer-content {
    height: 100vh;
    position:fixed;
    overflow-y:scroll;
}
```

How it looks like:

<img alt="preview" height="960" src="./img/preview.gif" width="443"/>

### Useful links

[Reed the discussion on _stack_**overflow**](https://stackoverflow.com/questions/69365869/prevent-select-input-on-ios-15-safari-from-hiding-and-showing-address-bar)

