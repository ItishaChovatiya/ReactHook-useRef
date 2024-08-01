
# React Hook: useRef

## Overview

`useRef` is a React Hook that allows you to persist values across renders without causing re-renders. It provides a way to access and interact with DOM elements directly or store mutable values that don’t trigger re-renders when updated.

## Features

- **Persist Values**: Store values across renders without causing re-renders.
- **Access DOM Elements**: Directly interact with DOM elements.
- **Immutable References**: Create a mutable reference that persists across the component’s lifecycle.

## Basic Usage

### Setting Up

1. **Import `useRef`**: Import `useRef` from React.

   ```jsx
   import React, { useRef } from 'react';
   ```

2. **Create a Ref**: Initialize the ref using `useRef`.

   ```jsx
   const myRef = useRef(null);
   ```

3. **Attach Ref to an Element**: Use the ref attribute to attach the reference to a DOM element.

   ```jsx
   <input ref={myRef} type="text" />
   ```

4. **Access the DOM Element**: Access the DOM element directly via the `current` property of the ref.

   ```jsx
   const focusInput = () => {
     myRef.current.focus();
   };
   ```

### Example

```jsx
import React, { useRef } from 'react';

function MyComponent() {
  const inputRef = useRef(null);

  const handleClick = () => {
    inputRef.current.focus();
  };

  return (
    <div>
      <input ref={inputRef} type="text" />
      <button onClick={handleClick}>Focus the input</button>
    </div>
  );
}

export default MyComponent;
```

## When to Use

- **Accessing DOM Elements**: For cases where you need to interact with a DOM element directly, such as focusing an input field.
- **Storing Mutable Values**: For storing values that don’t require re-rendering the component, such as timers or previous values.

## License

This React Hook documentation is licensed under the MIT License. See the `LICENSE` file for details.

## Contact

For questions or suggestions, please contact [Itisha Chovatiya](mailto:itishachovatiya7096@gmail.com).

---

Thank you for using the `useRef` Hook!
