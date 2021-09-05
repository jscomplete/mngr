## Learning Fullstack JavaScript Development: MongoDB, Node.js, React.js

Video Course: [samer.dev/mnr](https://samer.dev/mnr)

For an up-to-date configuration guide: [jscomplete.com/reactful](https://jscomplete.com/reactful)

For general help: [jscomplete.com/help](https://jscomplete.com/help)

### Reference Text

#### Babel

```js
module.exports = {
  presets: [
    "@babel/preset-env",
    ["@babel/preset-react", { runtime: "automatic" }],
  ],
};
```

#### Webpack

```js
module.exports = {
  devtool: "inline-source-map",
  entry: "./src/dom-render.js",
  output: {
    path: __dirname + "/public",
    filename: "bundle.js",
  },
  module: {
    rules: [
      {
        test: /\.js$/,
        exclude: /node_modules/,
        use: {
          loader: "babel-loader",
        },
      },
    ],
  },
};
```

#### ESLint

```js
module.exports = {
  parser: "babel-eslint",
  env: {
    es6: true,
    node: true,
    browser: true,
  },
  parserOptions: {
    ecmaVersion: "latest",
    ecmaFeatures: {
      impliedStrict: true,
      jsx: true,
    },
    sourceType: "module",
  },
  plugins: ["react", "react-hooks"],
  extends: [
    "eslint:recommended",
    "plugin:react/recommended",
    "plugin:react-hooks/recommended",
  ],
  settings: {
    react: {
      version: "detect",
    },
  },
  rules: {
    "react/react-in-jsx-scope": "off",
  },
};
```

#### Test Data

```json
{
  "contests": [
    {
      "id": 1,
      "categoryName": "Business/Company",
      "contestName": "Cognitive Building Bricks"
    },
    {
      "id": 2,
      "categoryName": "Magazine/Newsletter",
      "contestName": "Educating people about sustainable food production"
    },
    {
      "id": 3,
      "categoryName": "Software Component",
      "contestName": "Big Data Analytics for Cash Circulation"
    },
    {
      "id": 4,
      "categoryName": "Website",
      "contestName": "Free programming books"
    }
  ]
}
```

#### CSS

```css
.header {
  text-align: center;
}

.link {
  cursor: pointer;
}

.home-link {
  margin-top: 1em;
  color: #0000ee;
}

.contest-preview {
  margin: 1em;
  border: 1px solid #ccc;
}

.category-name {
  border-bottom: 1px solid #ccc;
  padding: 0.25em 0.5em;
  font-weight: bold;
  background-color: #eee;
}

.contest-name {
  padding: 0.5em;
}
```
