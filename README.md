# Sass Starter

An HTML and Sass boilerplate with a development server built in. Perfect for building static sites or creating pure css art.

## Prerequisites

- Have [Node.js](https://nodejs.org/en) downloaded and installed.
- Have [NPM](<https://en.wikipedia.org/wiki/Npm_(software)>) installed (included with Node.js)

## About The Starter

This project makes use of the [Gulp](https://gulpjs.com/) task runner. It is configured with two public tasks: `gulp sync`, which initializes a development server and `gulp build`, which creates a production build.

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

Remember not to make any changes to the `app/css` folder, as these will be overwritten when gulp compiles Sass to CSS.

### The Development Server

`gulp sync` will compile `.sass` and `.scss` files to CSS using the [gulp-sass](https://github.com/dlmanning/gulp-sass) package. It will then spin up a development server using [Browsersync](https://browsersync.io/docs/gulp) and continue to [watch](https://gulpjs.com/docs/en/getting-started/watching-files/#watched-events) your source files for changes and resync the browser on change.

### The Distribution Folder

`gulp build` will create a `public` folder and a production ready build inside of it containing your minified HTML and CSS output. By default, this folder is incldued in the `.gitignore` file.

### Deploying Your Static Site

#### Vercel Deployment

1. Create a free account with [vercel.com](https://vercel.com/new)
1. Import your project at [vercel.com/new](https://vercel.com/new)
1. Configure your project
   **Framework Preset:** `Other`
   **Root Directory:** `./`
1. Add build and output settings:
   **Build Command:** `gulp build`
   **Output Directory:** `public`
   **Install Command:** `npm install`
1. Click "Deploy" and wait for the initial build and deployment to complete.

### Opinionated Additions

- This template includes the [modern-normalize](https://github.com/sindresorhus/modern-normalize) css reset CDN. If you do not wish to use this reset, just remove it from `src/index.html`.
- This template makes use of `.scss` files, but it also supports `.sass` out of the box. If you wish to use `.sass`, just update the file extensions.
