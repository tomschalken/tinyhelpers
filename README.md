# TinyHelpers

## Find all elements that are wider than the viewport
`[...document.querySelectorAll('*')].filter(element => element.offsetWidth > window.innerWidth)`
