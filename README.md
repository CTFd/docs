# CTFd Docs

[![Documentation Status](https://api.netlify.com/api/v1/badges/6d10883a-77bb-45c1-a003-22ce1284190e/deploy-status)](https://docs.ctfd.io)

This is the repository for the official documentation and knowledge base for the CTFd ecosystem of services and tools. It can be viewed online at https://docs.ctfd.io/.

## Contributing

To contribute new changes/fixes to the docs, fork the repo, make your changes in a branch, and create an pull request against this repo.

### Local Setup

The docs are developed using [hugo](https://gohugo.io/) with the [docsy theme](https://github.com/google/docsy). These install instructions are written for OSX as a majority of development occurs there.

Javascript dependencies are managed with [yarn](https://yarnpkg.com/).

```
brew install hugo
git clone --recurse-submodules --depth 1 git@github.com:CTFd/docs.git
yarn install
hugo server
open http://localhost:1313/
```

The documentation is automatically built and deployed to https://docs.ctfd.io/ after being merged to master.
