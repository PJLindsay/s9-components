# s9-components

## Purpose

take deeper look at Components in Vue 3

## Concepts

- a better way to register components (Global vs Local)
- scoped style: keep styling for the local template only (non-global style)
- slots: allow us to receive HTML content (incl Vue features) from outside component
- scoped slots: allow some aspects of component to be customizable
- dynamic components: component allows us to swap in/out any component
- keep-alive: can be used with dynamic components so we don't lose input field data when we switch components
- teleport: built in component allows item to be rendered somewhere else in DOM structure (e.g. render in body      element (not deeply nested in HTML))
- working with fragments (multiple top-level elements allowed in Vue3)