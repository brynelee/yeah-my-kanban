# yeah-my-kanban
React Study demo project


## steps for making the project

### initialize the package.json file
npm init -y

### update configuration file of pakcage.json
"private": true,

### add version lock configuration by .nvmrc
16.17.1

### install vite
npm install -D vite

### config package.json

  "scripts": {
    "start": "vite dev --open", 
    "build": "vite build",

### create index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>React App</title>
  </head>
  <body>
    <noscript>You need to enable JavaScript to run this app.</noscript>
    <div id="root"></div>
  </body>
</html>

### install react
npm install react react-dom
npm install -D @vitejs/plugin-react

### create file of vite.config.js

import { defineConfig } from 'vite';
import react from '@vitejs/plugin-react';

export default defineConfig({
  plugins: [react()]
});

### isntall emotion
npm install @emotion/react
npm install -D @emotion/babel-plugin

### update vite.config.js
export default defineConfig({
  plugins: [
    react({
      jsxImportSource: '@emotion/react',
      babel: {
        plugins: ['@emotion/babel-plugin'],
      },
    }),
  ],
});

### import src/index.js & index.css to src/index.jsx & index.css


### import other src/* to src/components (component and css files)

### import context/

### install Types of React

npm install -D @types/react @types/react-dom

### install ESLint

npm init @eslint/config -y

### update package.json

"lint": "eslint './src/**/*.{js,jsx}'",