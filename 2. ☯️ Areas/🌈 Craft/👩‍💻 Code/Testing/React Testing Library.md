https://testing-library.com/docs/react-testing-library/intro/

# React Testing Library

By [[Kent C. Dodds]]

React Testing Library builds on top of DOM Testing Library by adding APIs for working with React components.

## Queries

https://testing-library.com/docs/queries/about

### getByRole

https://testing-library.com/docs/queries/byrole

#### Forms

[[2021-05-28]]

In order for the `getByRole()` API to work correctly with `form` elements, the forms must be named either with the HTML `name`, `aria-label`, or `aria-labelledby` attribute.

This was intentional, designed to follow the [W3 specification](https://www.w3.org/TR/html-aam-1.0/#details-id-42) for forms.

**Doesn't Work**

```jsx
// Form.js
<form>
  ...
</form>
```

```jsx
const { getByRole } = render(<Form />)
const form = getByRole('form')
```

**Works!**

```jsx
// Form.js
<form aria-label="Contact Form">
  ...
</form>
```

```jsx
const { getByRole } = render(<Form />)
const form = getByRole('form')
```

A better usage of `getByRole` is to provide a `option.name`. This allows you target specific elements as there may be multiple `form` elements on the page.

```jsx
const { getByRole } = render(<Form />)
const form = getByRole('form', { name: /Contact Form/i })
```


## Configure

### testIdAttribute

https://testing-library.com/docs/dom-testing-library/api-configuration/

[[2021-05-28]]

By default, when using the query `getByTestId`, React Testing Library looks for the HTML attribute of `data-testid`.

If you chose to use a different attribute, e.g. `data-automation-id`, you must `configure` React Testing Library so that `getByTestId` knows to look for that custom attribute.

**Example**

```jsx
import { configure } from '@testing-library/react';

configure({testIdAttribute: 'data-automation-id'});

// getByTestId('hello');
// ☝️ Should now look for `data-automation-id="hello"`
```

## Cheatsheet

👉 https://testing-library.com/docs/dom-testing-library/cheatsheet/