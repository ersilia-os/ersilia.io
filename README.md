# Ersilia website

This is the Git repository for the [Ersilia Hub](ersilia-hub.netlify.app) webiste (largely based on the awesome [Gridsome](gridsome.org) website)

## Install

Installation below may need `sudo` privileges.

1. Install Gridsome CLI tool
* Using YARN: `yarn global add @gridsome/cli`
* Using NPM: `npm install --global @gridsome/cli`

2. Create Gridsome project from GitHub
* `gridsome create ersilia.io https://github.com/ersilia-os/ersilia.io.git`
* `cd ersilia.io` to open folder
* `gridsome develop` to start local dev server

## Linting Markdown

Gridsome usese [markdownlint-cli](https://www.npmjs.com/package/markdownlint-cli) to enforce style consistency rules on the documentation. The linter runs automatically on every push and pull request via [GitHub Actions](https://docs.github.com/en/actions).

To install the linter on your machine, run the following:

```shell
npm install -g markdownlint-cli@0.23.2
```

You can check your changes for linter errors by running:

```shell
markdownlint '**/*.md' --ignore node_modules
```

The linter can automatically fix certain classes of failure. To accept these fixes, run:

```shell
markdownlint '**/*.md' --ignore node_modules --fix
```

## Deploy on Netlify

We deploy this website using [Netlify](netlify.com).

* Run command: `gridsome build`
* Folder: `dist`
