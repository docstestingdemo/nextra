

  # How to Use React Components in Nextra

Nextra allows you to seamlessly integrate React components into your Markdown files. Here's how you can do it:

1. Import the React component at the top of your MDX file:

import MyComponent from '../components/MyComponent'

2. Use the component directly in your Markdown:

## My Section

Here's my custom React component:

<MyComponent />

You can also pass props to your components:

<MyComponent prop1="value1" prop2={42} />

3. You can mix Markdown and React components freely:

# My Page

This is regular Markdown content.

<MyComponent />

More Markdown content here.

4. For dynamic content, you can use React hooks and state:

import { useState } from 'react'

export function Counter() {
  const [count, setCount] = useState(0)
  return (
    <button onClick={() => setCount(count + 1)}>
      Clicked {count} times
    </button>
  )
}

## Interactive Component

Here's a counter:

<Counter />

5. You can also use built-in Nextra components:

import { Callout } from 'nextra/components'

<Callout type="info">
  This is an info callout using a Nextra component.
</Callout>

Remember that when using React components in MDX, the normal Markdown syntax still works for the rest of your content. This allows you to create rich, interactive documentation with ease.

  