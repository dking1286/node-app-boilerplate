# Node App Boilerplate

A project skeleton for Node.js server projects, including Babel,
Eslint, Flow, Gulp, and Tape setup.

## Initial Setup

- Create directories `src`, `dist`, and `spec` in the root directory.
- Inside `spec`, create a folder `setup`.

## How to Use

- All source files that you want transpiled should be placed inside the
  `src` directory.
- Any files containing test setup information (for example, invoking
  `require('babel-register')` or initializing the database connection)
  should be placed inside `spec/setup`. All files in this folder will be run
  before any of the tests themselves are run.
- Any files containing tests should be placed directly inside the `spec`
  directory.
- To run the build process for development, use `npm run build:watch`. This
  will transpile everything inside the `src` directory and create an exact
  mirror of the directory structure inside the `dist` directory. Note that
  this build process will *not* bundle the code.
- The main file should be placed at `src/index.js`. Using `npm run start:dev` or
  `npm run start:prod` (for development or production, respectively) will run
  the file `dist/index.js`, the transpiled version of the main file.
