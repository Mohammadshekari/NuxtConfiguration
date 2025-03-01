# Create Nuxt Project

Node.js - 18.x or newer (but we recommend the active LTS release)

```sh
npm -v
```

Open a terminal (if you're using Visual Studio Code, you can open an integrated terminal) and use the following command to create a new starter project:

```sh
npx nuxi@latest init <project-name>
```
√ Which package manager would you like to use? ```npm ```

√ Initialize git repository? ```Yes```

✨ Nuxt project has been created with the v3 template. Next steps:
```
cd <project-name>
npm run dev
```

---
# Project Folders for Nuxt

this folders will be auto used:

```
project:
  |- assets
  |- components
  |- composables
  |- layouts
  |- middleware
  |- pages
  |- plugins
  |- types
```

---
# Add NuxtUI

Install nuxtui on the project:
```sh
npx nuxi@latest module add ui
```
it will add `'@nuxt/ui'` to `nuxt.config.ts` modules list.

create tailwind file in project folder `tailwind.config.js` with this content:
```js
/** @type {import('tailwindcss').Config} */
module.exports = {
    content: [
        "./index.html",
        "./**/*.{vue,js,ts}"
    ],
    theme: {
        extend: {},
    },
    plugins: [],
}
```
it will recognize css classes.

then create css file `assets/css/tailwind.css` with this content:
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```
to import default tailwind css codes.

