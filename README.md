# react-value

An easy easy way to wrap controlled components that provide `value` and `onChange` props with state.

Makes your components behave like React input components.

## Install

```
yarn add react-value
```

## Use

You can either use the `Value` component, which takes a `render` prop:

```jsx
import { Value } from 'react-value';

<Value
  defaultValue={defaultValue} // optional
  onChange={(newValue) => null} // optional
  render={(value, onChange) => (
    <MyInput onChange={onChange} value={value} />
  )}
/>
```

..or for repeated use, you can use the `withValue` HOC:

```jsx
import { withValue } from 'react-value';

const MyInputWithValue = withValue(MyInput);

<MyInputWithValue defaultValue="Hello World" />
```

# License

Copyright (c) 2017 Jed Watson. MIT Licensed.
