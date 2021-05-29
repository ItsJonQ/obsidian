# Jest

## Forms

### Named Values

[[2021-05-28]]

There appears to be some difficulty when working with `form.valueName` values in React and Jest. It seems like updating values using `fireEvent` from [[React Testing Library]] doesn't register them onto the `form` HTML element.
