<img alt="phuwn avatar" title="phuwn avatar" src="https://github.com/phuwn/phuwn.wtf/blob/master/static/media/do.png" width="140"> </br>

# [phuwn.wtf](https://phuwn.wtf)

[![Netlify Status](https://api.netlify.com/api/v1/badges/4817c355-fe35-4023-be0b-c4e69a6c5557/deploy-status)](https://app.netlify.com/sites/phuwnblog/deploys)

A personal blog of a tech lover. Welcome to my huge and crazy world.

---

Forked from [Gatsby starter lumen](https://github.com/alxshelepenok/gatsby-starter-lumen).

Inspired by [tiggreen/tik.dev](https://github.com/tiggreen/tik.dev).

## Table of contents

- [Features](http://github.com/phuwn/phuwn.wtf#features)
- [Quick Start](http://github.com/phuwn/phuwn.wtf#quick-start)
- [Deploy with Netlify](http://github.com/phuwn/phuwn.wtf#deploy-with-netlify)
- [Folder Structure](http://github.com/phuwn/phuwn.wtf#folder-structure)
- [License](http://github.com/phuwn/phuwn.wtf#license)

## Features

- [WIP] Personal blog [`/`](https://phuwn.wtf/)
  - Some of my post on `/posts/${pid}`
  - Find posts with category `/category/${cid}`
  - Find posts with tag `/tag/${tid}`
- A short introduction about me [`/about`](https://phuwn.wtf/about)
- My knowledge base [`/bookshelf`](https://phuwn.wtf/bookshelf)
- Some of my highlighted projects [`/projects`](https://phuwn.wtf/projects)
- A bit about my relax corner hehe [`/chill`](https://phuwn.wtf/chill)
- Contact info [`/contacts`](https://phuwn.wtf/contacts) including those social account on menu

## Quick Start

#### Installation

```sh
# Create a new Gatsby site
npm install -g gatsby-cli
gatsby new phuwn.wtf https://github.com/phuwn/phuwn.wtf
cd phuwn.wtf
npm install
```

#### Run on develop environment

```sh
gatsby develop
# Your site is now running at `http://localhost:8000`!
```

#### Using custom Express.js instead

```sh
gatsby build
node server.js
# Your site is now running at `http://localhost:3000`!
```

## Deploy with Netlify

[Netlify](https://netlify.com) CMS can run in any frontend web environment, but the quickest way to try it out is by running it on a pre-configured starter site with Netlify. Use the button below to build and deploy your own copy of the repository:

<a href="https://app.netlify.com/start/deploy?repository=https://github.com/phuwn/phuwn.wtf" target="_blank"><img src="https://www.netlify.com/img/deploy/button.svg" alt="Deploy to Netlify"></a>

After clicking that button, you’ll authenticate with GitHub and choose a repository name. Netlify will then automatically create a repository in your GitHub account with a copy of the files from the template. Next, it will build and deploy the new site on Netlify, bringing you to the site dashboard when the build is complete. Next, you’ll need to set up Netlify’s Identity service to authorize users to log in to the CMS.

## Deploy to Github Pages

To deploy to github pages, simply do the following:

- Ensure that your `package.json` file correctly reflects where this repo lives
- Change the `pathPrefix` in your `config.js`
- Run the standard deploy command

```sh
npm run deploy
```

#### Access Locally

```
$ git clone https://github.com/[GITHUB_USERNAME]/[REPO_NAME].git
$ cd [REPO_NAME]
$ yarn
$ npm run develop
```

To test the CMS locally, you'll need run a production build of the site:

```
$ npm run build
$ gatsby serve
```

## Folder Structure

```
└── content
    ├── pages
    └── posts
└── static
    ├── admin
    └── media
└── src
    ├── assets
    │   └── scss
    │       ├── base
    │       └── mixins
    ├── cms
    │   └── preview-templates
    ├── components
    │   ├── Feed
    │   ├── Icon
    │   ├── Layout
    │   ├── Page
    │   ├── Pagination
    │   ├── Post
    │   │   ├── Author
    │   │   ├── Comments
    │   │   ├── Content
    │   │   ├── Meta
    │   │   └── Tags
    │   └── Sidebar
    │       ├── Author
    │       ├── Contacts
    │       ├── Copyright
    │       └── Menu
    ├── constants
    ├── templates
    └── utils

```

## License

The MIT License (MIT)

Copyright (c) 2016-2020 Alexander Shelepenok

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
