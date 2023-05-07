# Sass Starter

A starter template for [Sass](https://sass-lang.com/) projects with a development server built in.

## Prerequisites

- Have [Node.js](https://nodejs.org/en) downloaded and installed.
- Have [NPM](<https://en.wikipedia.org/wiki/Npm_(software)>) installed (included with Node.js)

## About The Starter

This project makes use of the [Gulp](https://gulpjs.com/) task runner. It is configured with two public tasks: `gulp sync` and `gulp build`.

```
Tasks for sass-starter
├─┬ sync
│ └─┬ <series>
│   ├── compileCss
│   └── develop
└─┬ build
  └─┬ <parallel>
    ├─┬ <series>
    │ ├── compileCss
    │ └── minifyCss
    └── minifyHtml
```

Run `gulp --tasks` to see this breakdown in your own terminal.

`gulpfile.js` is well commented to explain what each function does and it includes links to the official docs that were used to build this template.

### The Development Server

`gulp sync` will compile `.sass` and `.scss` files to CSS using the [gulp-sass](https://github.com/dlmanning/gulp-sass) package. It will then spin up a development server using [Browsersync](https://browsersync.io/docs/gulp) and continue to [watch](https://gulpjs.com/docs/en/getting-started/watching-files/#watched-events) your source files for changes and resync the browser on change.

### The Distribution Folder

`gulp build` will create a `public` folder and a production ready build inside of it containing your minified HTML and CSS output.
