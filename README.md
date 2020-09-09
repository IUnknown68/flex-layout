# flex-layout

Helper (css) for creating flex-box-based layouts.

## What it is

A bunch of css-classes, bound to custom elements (`fl-box`, `fl-row`, `fl-column`) to organize HTML in rows and columns. It aims for simplicity, and for keeping the markup readable. Use them to create (pagefilling) layouts.

## What it is not

- A complete wrapper for flex-box.
- A layout-framework.
- Something to solve all your layout problems.

## How to use

Get `flex-layout.css` in your css, page, sass or whatever you use. Now compose your layout of `fl-box`, `fl-row`, `fl-column`.

If you need a pagefilling layout, you should give your `html`, `body` and possibly all parents of your layout the following style:

```css
margin: 0;
padding: 0;
height: 100%;
width: 100%;
overflow: hidden;
```

**Note**: On mobiles, this might prevent reloading the page via pull-down. If you need to allow, set `overflow:visible` on both `html` and `body`.

Also on mobiles, you might or might not want the built-in browser UI to scroll away when scrolling down. If so, set the `height` in the css above to `100vh` instead of `100%`.

For an example, see `example.html`.
