# Angular-ELectron-Demo

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 8.0.6.

# Installed Packages

1. npm install electron --save-dev
2. npm install electron-packager -g
3. npm install electron-packager --save-dev

# Steps to convert app

1. In `src/index.html` change <base href="/"> to <base href="./">

2. Install electron `npm install electron --save-dev`

3. Create main.js in root of the project (not in src) (this is where createWindow() code goes)

4. Ensure main.js points to `dist/index.html` (not just index.html)

5. Add "main":"main.js", in `scripts` section of the `package.json`

6. Add below code in `scripts` section of the `package.json`

"electron": "electron .", // <-- run electron 
"electron-build": "ng build --prod && electron ." // <-- build app, then run electron `

7. run/debug the app with:
   `npm run electron-build`

8. to build the app:
`npm install electron-packager -g​​`
`npm install electron-packager --save-dev`

# Build
9. then run:

for Windows
`electron-packager . --platform=win32​`

for Mac
`electron-packager . — platform=darwin`

