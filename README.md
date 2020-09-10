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

If you need a pagefilling layout, you should give your `html`, `body`, the root of your layout, and possibly all parents the following style:

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

## Reference

### Elements

#### fl-row

Organizes its children in a row. An `fl-box` with `display: flex` and `flex-direction: row`.

#### fl-column

Organizes its children in a column. An `fl-box` with `display: flex` and `flex-direction: column`.

#### fl-box

A cell in a flex-layout.

### Attributes

#### stretch

Stretches a cell (or row, column) to the remaining width / height (`flex: 0 1 100%`)

#### fixed

Forbids a cell (or row, column) to grow or shrink (`flex: 0 0 auto`).

#### center

Use on a row when you want to center the children vertically.

#### scroll

Allows a cell (or row, column) to have a scroll-bar (`overflow: auto`).
