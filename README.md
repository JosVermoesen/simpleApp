# simpleApp Ionic

## Install and update the frameworks

- [Install NodeJS](https://nodejs.org/). Hint: eventually install and use [nvm](https://medium.com/@Joachim8675309/installing-node-js-with-nvm-4dc469c977d9) for easy installing and/or switching between node versions
- Check node: `node -v`
- Check node package manager: `npm -v`

- [Angular CLI](https://www.npmjs.com/package/@angular/cli): `npm i -g @angular/cli`

- Remove previous Ionic (eventualy): `npm i -g @ionic/cli`
- Install latest Ionic: `npm i -g @ionic/cli`
- Check Ionic version: `ionic -v`

## Getting started for users

Create the application: `ionic start simpleApp blank --type=angular --capacitor`
Adding a page with a name 'details': `ionic g page details`
Add capacitor platform one: `npm install @capacitor/android`

#### Do not forget to update regularly Angular for your Ionic project

- Upgrading to latest Angular: `ng update @angular/core @angular/cli`
- Latest ionic toolkit: `npm i @ionic/angular-toolkit@latest`

### Serving our app code on github

- Clone this repository: `git clone https://github.com/JosVermoesen/simpleApp.git`.
- Run `npm install` inside the project root.
- Run `ionic serve` in a terminal from the project root.
- Or use `ionic lab` if you want to check side by side version of android and ios
- Profit. :tada:

## During development

- Initialize capacitor: `npx portfolio be.vsoft.portfolio`

- Initialize app: `npx cap init`

- Add Android platform: `npx cap add android`
- Build command: `ionic cap build android`

- First build (important!): `ionic build` or production build: `ionic build --prod`
- After every build (important!): `npx cap copy`

- Open Android IDE (after latest build): `npx cap open android`
- Or use life reload: `ionic cap run android --l --external`
- Profit. :tada:

## NPM packages used for this app

- [@ngx-translate/core](https://www.npmjs.com/package/@ngx-translate/core): `npm i @ngx-translate/core`
- [@ngx-translate/http-loader](https://www.npmjs.com/package/@ngx-translate/http-loader): `npm i @ngx-translate/http-loader`
- [jsqr](https://www.npmjs.com/package/jsqr): `npm i jsqr`
- [x](https://github.com/techiediaries/ngx-qrcode): `npm i @techiediaries/ngx-qrcode`

- install all packages in one commandline: `npm i @ngx-translate/core @ngx-translate/http-loader jsqr @techiediaries/ngx-qrcode`

## Updating

### Ionic

- Info on current Ionic version: `Ionic -v`
- Updating Ionic globaly: `npm update -g ionic`
- Updating your project: `ionic lib update`
- Get available versions on npm: `npm info ionic`
- Get all info on your current ionic, capacitor, used framework and npm: `ionic info`

### Angular

This app is on Angular 11. Update to latest Angular 11 with:
`ng update @angular/cli@11 @angular/core@11`

Follow the instructions eventualy for fixes

## From Angular 10+ warnings

In angular.json, to avoid CommonJs warnings, add **allowedCommonJsDependencies** in the options section for **qrcode**:

```bash
"builder": "@angular-devkit/build-angular:browser",
          "options": {

            "allowedCommonJsDependencies": [
              "qrcode",
              "url"
            ],

```

## VS CODE Extensions 2021

indent rainbow
rest client
css peek (ctrl+hover)

## tsconfig.json changes for using version stamp in app

Before building, set resolveJsonModule to 'true' :

```bash
"compilerOptions": {

    "resolveJsonModule": true,

```

## Best practices: use lazy loading modules

- Generate modules ex. a hosting module: `ng generate module modules/hosting --route hosting --module app.module`
- Generate modules ex. a contact module: `ng generate module modules/contact --route contact --module app.module`

## Good practice: Updating Angular as needed

This app is on Angular 11. Update to latest Angular 11 with:
`ng update @angular/cli@11 @angular/core@11`

Follow the instructions eventualy for fixes
