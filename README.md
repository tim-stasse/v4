# bootstrap-styled

bootstrap-styled npm package.

**Master**

[![build status](https://module.kopaxgroup.com/styled-components/bootstrap-styled/badges/master/build.svg)](https://module.kopaxgroup.com/styled-components/bootstrap-styled/commits/master)
[![coverage report](https://module.kopaxgroup.com/styled-components/bootstrap-styled/badges/master/coverage.svg)](https://module.kopaxgroup.com/styled-components/bootstrap-styled/commits/master)

**Dev**

[![build status](https://module.kopaxgroup.com/styled-components/bootstrap-styled/badges/dev/build.svg)](https://module.kopaxgroup.com/styled-components/bootstrap-styled/commits/dev)
[![coverage report](https://module.kopaxgroup.com/styled-components/bootstrap-styled/badges/dev/coverage.svg)](https://module.kopaxgroup.com/styled-components/bootstrap-styled/commits/dev)

## Table of Contents

  - [Changelog](#changelog)
  - [Reminders](#reminders)
  - [Quick start](#quick-start)
  - [Release](#release)

---

## Changelog

  - View [Changelog](CHANGELOG.md)

## Reminders

**⚠️ When using this plugin, you must import in the first line of your application javascript entry file `babel-polyfill`: ⚠️**
  
    import "babel-polyfill";
    
To enable ES features in older browsers, you MUST include in the package.json

    "browserslist": ["ie >= 9", "last 2 versions"]
    // or
    "browserslist": ["ie >= 10", "last 2 versions"]

## Quick start

Clone project

    git clone ssh://git@module.kopaxgroup.com:20024/styled-components/bootstrap-styled.git

Install dependencies

    npm install

Build project

    npm run build
    
Run unit test
     
    npm test
    
Watch unit test
     
    npm run test:watch

Watch the `/dist` directory

    npm run build:dist:watch

Watch the `/lib` directory

    npm run build:lib:watch

# Contribute

`master` is used to release the version. 

- `master` only accept merge requests from `dev`

`dev` is the developement branch. It should be used by developers for applying their merge requests.

If you wish to implement new functionalities you need to do a merge request including your change on the `dev` branch.

    git checkout dev
    git checkout $(whoami)-dev
    git push -u origin $(whoami)-dev 

You can now start working on your branch. Don't forget to check `Delete branch when merged`.

## Release

Merge `dev` into `master` will release a new version and prepare a new version in `dev`.

To release a new version, edit the [Changelog](CHANGELOG.md) and set the version in `package.json` and merge your change into `master`.

**⚠️ if you are releasing on a git repository instead of a npm repository, **DO NOT** forget to remove `build`, and `dist` from the `.gitignore` ⚠️**

    sed -i "/lib\|dist/d" .gitignore

