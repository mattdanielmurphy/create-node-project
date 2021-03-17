## create-node-project

A tool I created for myself to create new node projects.

## usage

`create-node-project [project | project-directory]`

### Features

- configs:

  - gitignore
  - prettier

- node_modules won't sync with iCloud thanks to the [.nosync alias fix](https://davidsword.ca/prevent-icloud-syncing-node_modules-folder/)

## steps to create

- require first argument: name
- get project name from first argument
- git clone project-template folder: `gh repo clone mattdanielmurphy/create-node-project`
- create git repo and project folder

- `npm init -y` & install packages
- create node_modules.nosync & alias: `mkdir node_modules.nosync && ln -s node_modules.nosync node_modules`

## project-template

Include:

- gitignore with `node_modules*`
- prettier config

## requirements

- github-cli `npm i -g gh`

## to do

- use typescript
- use cli framework
- fix using a dot as project/dir name
- add tests! (will make it easier for below)
- make it so you can do the following `create-node-project { directory | project-name }` with:
  - subdirectory that matches project-name
  - `.`, setting project-name to that of parent dir
  - project-name, creating a project dir with that name
  - make project dir follow naming convention: `Project Name`
- add testing to new projects (jest)
