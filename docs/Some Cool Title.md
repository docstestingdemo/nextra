

  # Using React Components in MDX

MDX allows you to seamlessly integrate React components into your Markdown content. This powerful feature enables you to create dynamic and interactive documentation.

## Basic Usage

To use a React component in your MDX file, simply import it and then use it like you would in a JSX file:

```jsx
import { MyComponent } from './components/MyComponent'

# Welcome to My Page

Here's my custom component:

<MyComponent />
```

## Passing Props

You can pass props to your components just like in regular React:

```jsx
import { Button } from './components/Button'

# Interactive Button

<Button color="blue" onClick={() => alert('Clicked!')}>
  Click me
</Button>
```

## Using Components with Markdown

MDX allows you to mix Markdown and components freely:

```jsx
import { Callout } from 'nextra/components'

# Important Information

Regular Markdown content goes here.

<Callout type="info">
  This is an important note rendered using the Callout component.
</Callout>

More Markdown content...
```

## Creating Layouts

You can use components to create custom layouts for your MDX pages:

```jsx
import { Layout } from './components/Layout'

export default ({ children }) => <Layout>{children}</Layout>

# Page Content

This content will be wrapped in the Layout component.
```

## Dynamic Content

Leverage React's state and effects to create dynamic content:

```jsx
import { useState } from 'react'

export function Counter() {
  const [count, setCount] = useState(0)
  return (
    <button onClick={() => setCount(count + 1)}>
      Clicked {count} times
    </button>
  )
}

# Interactive Counter

<Counter />
```

## Best Practices

1. Keep components simple and focused.
2. Use TypeScript for better type checking and autocompletion.
3. Leverage Nextra's built-in components when possible.
4. Use ESM import syntax for better compatibility.

By combining the simplicity of Markdown with the power of React components, MDX allows you to create rich, interactive documentation that enhances the user experience.

  