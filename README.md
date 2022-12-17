# VSCode - ESLint, Prettier & Airbnb Setup for Node.js Projects

### 1. Install ESLint & Prettier extensions for VSCode

Optional - Set format on save and any global prettier options

### 2. Install Packages

```
npm i -D eslint prettier eslint-plugin-prettier eslint-config-prettier eslint-config-airbnb-base eslint-plugin-node eslint-config-node
```

### 3. Create .prettierrc for any prettier rules (semicolons, quotes, etc)

```
{
  "trailingComma": "es5",
  "tabWidth": 2,
  "semi": true,
  "singleQuote": true
}
```

### 4. Create .eslintrc.json file (You can generate with npx eslint --init)

```
{
  "env": {
    "commonjs": true,
    "es6": true,
    "node": true
  },
  "extends": ["airbnb-base", "prettier", "plugin:node/recommended"],
  "globals": {
    "Atomics": "readonly",
    "SharedArrayBuffer": "readonly"
  },
  "parserOptions": {
    "ecmaVersion": 2018
  },
  "plugins": ["prettier"],
  "rules": {
    "prettier/prettier": "error",
    "no-unused-vars": "warn",
    "no-console": "off",
    "func-names": "off",
    "no-plusplus": "off",
    "no-process-exit": "off",
    "class-methods-use-this": "off"
  }
}
```

### Also Add Your Setting

- Go to setting and and Click Workspace Like this 👇👇

![Logo](https://i.ibb.co/4NKrZsp/aa.png)

- Click This Icon 👇👇

![Logo](https://i.ibb.co/bFZs1RT/1.png)

- And Also Past Code (setting.json) File.

```

{
  // config related to code formatting
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true,
  "[javascript]": {
    "editor.formatOnSave": false,
    "editor.defaultFormatter": null
  },
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true,
    "source.organizeImports": true
  },
  "eslint.alwaysShowStatus": true
}

```

# Now Time to Write Code .. Have a Nice Day ❤ 

### Reference

- ESLint Rules - https://eslint.org/docs/rules/
- Prettier Options - https://prettier.io/docs/en/options.html
- Airbnb Style Guide - https://github.com/airbnb/javascript
