# SVG attributes

## Namespace

- xmlns => XML Name Space
- To let the **user agent** know how to treat each tag properly

For instance, `title` inside name space **html**

```html

<html lang="en" xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title>1.1 - Setting up our app</title>
</head>
</html>
```

and inside namespace **svg**

```html

<svg xmlns="http://www.w3.org/2000/svg">
    <title>My SVG document</title>
</svg>
```

are treated differently.

### xmlns:xlink

```html
<a href="https://developer.mozilla.org/">Link</a>

<svg
        xmlns="http://www.w3.org/2000/svg"
        xmlns:xlink="http://www.w3.org/1999/xlink"
>
    <a href="https://developer.mozilla.org/">Link</a>
    <title>My SVG document</title>
</svg>
```

- https://developer.mozilla.org/en-US/docs/Web/SVG/Namespaces_Crash_Course

### Namespace are removable

This would be fine on modern browsers.

```html

<svg>
    <circle cx="300" cy="300" r="300"/>
</svg>
```

---

## Width & height

```html

<svg width="600" height="600">
    <circle cx="300" cy="300" r="300"/>
</svg>
```

- Viewport of the SVG
  ![plane-window.png](images/plane-window.png)
- Could be set via CSS, but it is a good practice to have the attribute as a fallback.

```css
svg {
    width:600px;
    height:600px;
}
```

---

## Viewbox

- Telescope
  ![telescope.png](images/telescope.png)
- Can pan and zoom
- `min-x | min-y | width | height`
    - min-x = 100 => add 100 unit to the right of viewport
    - min-y = 100 => add 100 unit to the bottom of viewport
    - width = 1200, height = 1200 => move the viewport further twice