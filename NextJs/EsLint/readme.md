## ESLint

### Installation:
```bash
npm install --save-dev eslint eslint-config-airbnb eslint-plugin-import eslint-plugin-react
```

**Configuration:**
<p>Create an <b>.eslintrc.json</b> file in your project root and add the following configuration:</p>

```JavaScript
{
  "extends": ["eslint:recommended", "airbnb", "plugin:import/errors", "plugin:import/warnings", "plugin:react/recommended", "next/core-web-vitals"],
  "parser": "babel-eslint",
  "parserOptions": {
    "ecmaFeatures": {
      "jsx": true
    },
    "sourceType": "module"
  },
  "env": {
    "browser": true,
    "node": true,
    "es2021": true // Adjust for your target ECMAScript version
  },
  "plugins": ["import", "react"],
  "rules": {
    "no-unused-vars": [
      "error",
      { "varsIgnorePattern": "^_" } // Allow ignoring variables starting with underscore for private usage
    ],
    "no-console": "warn", // Allow console logs with a warning
    "react/prop-types": 0, // Disable prop-types for simplicity (consider using TypeScript for type safety)
    "import/extensions": ["error", "ignorePackages", { "js": "always", "jsx": "always" }],
    "import/order": ["next", "groups", "builtin", "external", "internal", "parent", "sibling", "index"], // Import ordering (optional)
    "react/jsx-filename-extension": [1, { "extensions": [".js", ".jsx", ".ts", ".tsx"] }] // Allow JSX in all relevant extensions
    // Add or modify other ESLint rules as needed
  }
}

```

<p>This configuration extends Airbnb's style guide with React-specific rules and allows console logs with a warning. You can adjust the rules to your preferences.</p>

### Setting Up Script (Optional):

<p>For convenience, you can create a script in your package.json to automate formatting:</p>

```JSON
{
  "scripts": {
    "format": "prettier --write . && eslint ."
  }
}
```

<p>Now you can run "<b>npm run format</b>" to format your files.</p>

### Recommended Practices

<ul>
<li><b>Consistent Naming:</b> Enforce consistent naming conventions (e.g., PascalCase for components, camelCase for variables) using ESLint or Prettier rules.</li>
<li><b>Line Length:</b> Maintain a reasonable line length (e.g., 120 characters) using Prettier.</li>
<li><b>Spacing:</b> Use consistent indentation and spacing styles to improve readability.</li>
<li><b>Semicolons:</b> Decide on and enforce semicolon usage (e.g., Prettier can handle both styles).</li>
<li><b>Quotes:</b> Choose single or double quotes and stick with that style throughout the project.</li>
</ul>

### Additional Tips

<ul>
<li>Consider using code formatters for other file types (e.g., Prettier for JavaScript, JSON, etc.).</li>
<li>Explore linters like ESLint for JavaScript-specific code quality checks.</li>
<li>Integrate formatting and linting tools into your build process to ensure consistent code style throughout development.</li>
</ul>
