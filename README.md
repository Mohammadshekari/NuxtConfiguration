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
        "./pages/**/*.{vue,js,ts}",
        "./components/**/*.{vue,js,ts}",
        "./layouts/*.{vue,js,ts}"
    ],
    theme: {
        extend: {
            colors: {
              jade: { // Created with https://uicolors.app/create
                50: "#effef7",
                100: "#dafeef",
                200: "#b8fadd",
                300: "#81f4c3",
                400: "#43e5a0",
                500: "#1acd81",
                600: "#0fa968",
                700: "#108554",
                800: "#126945",
                900: "#11563a",
                950: "#03301f",
              },
              'persian-blue': {
                '50': '#eef6ff',
                '100': '#d9e9ff',
                '200': '#bcdaff',
                '300': '#8ec3ff',
                '400': '#58a2ff',
                '500': '#327dff',
                '600': '#1b5cf5',
                '700': '#1344d8',
                '800': '#173ab6',
                '900': '#19358f',
                '950': '#142257',
                }
            }
        },
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

now your Nuxt UI is Ready ✅ you can test with replace this code to your `app.vue` file
```vue
<template>
  <div>
    <UContainer class="my-5">
      <UButton label="Hi Wassap" color="primary"/>
      <br>
      <UIcon size="40" name="i-heroicons-arrow-trending-up"/>
    </UContainer>
  </div>
</template>
```
now you even can use `heroicons` in your app.

create `app.config.ts` to change global tailwind css settings:
```js
export default defineAppConfig({
    ui: {
        primary: 'cyan',
        gray: 'cool',
    }
})
```

