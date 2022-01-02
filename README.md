This repo is an example using tailwindcss with mint.

The steps are:

1. Create tailwind.config.js file on the root with the following content:

```js
module.exports = {
  content: ['./source/**/*.{html,js,mint}'],
  theme: {
    extend: {},
  },
  plugins: [],
};
```

2.  Create a source/main.css file with the following content:

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

3.  Create a tasks/start.sh script with the following content:

```sh
npx concurrently "mint start" "npx tailwindcss -i ./source/main.css -o ./assets/style.css --watch"
```

4.  Run the script:

```sh
  ./tasks/start.sh
```

You can use another tool for step 3.
