## Prettier

### Installation:
```bash
npm install --save-dev prettier
```

**Configuration:**
<p>Create a **.prettierrc** file in your project root with the following content:</p>

```
{
  "singleQuote": true,
  "semi": true,
  "trailingComma": "all",
  "arrowParens": "avoid",
  "printWidth": 80,
  "tabWidth": 4,
  "useTabs": false,
  "endOfLine": "auto"
}
```

**Ignore File (Optional but recommended)**
<p>Create a **.prettierignore** file in your project root with the following content:</p>

```
node_modules/
public/
.next/
build/
# Ignore all files ending with .min.css
*.min.css
```
