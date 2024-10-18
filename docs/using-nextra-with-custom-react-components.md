

  # Using Nextra with Custom React Components

Nextra allows you to seamlessly integrate custom React components into your Markdown content. Here's how you can do it:

1. Create your custom React component:

```jsx
// components/MyCustomComponent.js
import React from 'react';

const MyCustomComponent = ({ children }) => {
  return (
    <div style={{ border: '1px solid #ccc', padding: '10px' }}>
      ### Custom Component

      {children}
    </div>

  );
};

export default MyCustomComponent;
```

2. Import and use the component in your MDX file:

```mdx
import MyCustomComponent from '../components/MyCustomComponent';

# Page Title

Here's some regular Markdown content.

<MyCustomComponent>
  This is inside my custom component!
</MyCustomComponent>

More Markdown content...
```

3. If you want to use the component across multiple pages, you can add it to the `components` option in your Nextra configuration:

```js
// next.config.js
const withNextra = require('nextra')({
  theme: 'nextra-theme-docs',
  themeConfig: './theme.config.jsx',
  mdxOptions: {
    components: {
      MyCustomComponent: './components/MyCustomComponent'
    }
  }
});

module.exports = withNextra();
```

Now you can use `<MyCustomComponent>` in any MDX file without importing it.

4. You can also use dynamic components with the `dynamic` import from Next.js:

```mdx
import dynamic from 'next/dynamic';

const DynamicComponent = dynamic(() => import('../components/DynamicComponent'));

# Page with Dynamic Component

<DynamicComponent>
  This component was loaded dynamically!
</DynamicComponent>
```

5. For more complex scenarios, you can create a custom theme that includes your components:

```jsx
// theme.jsx
import { ThemeProvider } from 'next-themes';
import MyCustomComponent from './components/MyCustomComponent';

export default function Theme({ children }) {
  return (
    <ThemeProvider attribute="class">
      {children}
      <MyCustomComponent />
    </ThemeProvider>
  );
}
```

Then use this theme in your Nextra configuration.

By following these steps, you can easily integrate and use custom React components within your Nextra documentation.

  