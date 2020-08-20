# TinyHelpers

## Find all elements that are wider than the viewport
```
[...document.querySelectorAll('*')].filter(element => element.offsetWidth > window.innerWidth)
```

## Find all elements that intersect with a specific point in the viewport

```
const whatsHere = (x, y) => (
    [...document.querySelectorAll('*')].filter(element => {
        const { top, bottom, left, right } = element.getBoundingClientRect()
        return left <= x && right >= x && top <= y && bottom >= y
    })
)
```

then

```
whatsHere(150, 75)
```
