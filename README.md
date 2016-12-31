# gswg-project
A repository for the Getting Started With Grunt project from Chapter 4


## Introduction

Use Grunt to cerate the build for an optimized single-page application

A common use-case for Grunt is static websites. Static websites are growing in popularity, as the web development industry requires ever-increasing levels of scalability. Static files can be hosted very cheaply on a cloud service such as Amazon's S3. Static files don't put much load on the server, and the load on the server can be reduced even more by moving as much logic as possible onto the client (Single Page Application). This reduces cost and increases scalability.


## Initial Setup

```sh
cd C:\Projects
mkdir gswg-project
cd gswg-project
mkdir src
npm init
npm install --save-dev grunt
echo "module.exports = function(grunt) {};" > Gruntfile.js
npm install --save-dev grunt-contrib-coffee grunt-contrib-jade grunt-contrib-stylus
```

## Transcompile languages

Help to mangage the complexity of the application. Files can be split up and organised logically. Provide minimalist syntax and cleaner code.

- CoffeeScript (alternatives: TypeScript, Dart)
- Stylus (alternatives: Sass, LESS)
- Jade (alternatives: Haml, EJS)

Programs that perform transcompilation are called preprocessors. The grunt tasks are just thin wrappers around a preprocessor.


## Source Files

Three subdirectories (with language agnostic names):
- scripts
- styles
- views

## Build Files

The separation between src and build directories is important. The contents of build is temporary and overwritten often. Only the src files are intended to be modified manually. The build directory should be ignored by version control.

## Assets Optimization: additional transformations on the result

```sh
npm install --save-dev grunt-contrib-uglify
npm install --save-dev grunt-contrib-cssmin
npm install --save-dev grunt-contrib-htmlmin
```
