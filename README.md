# DxE Tech documentation

This guide explains how DxE tech works. To edit this guide, go to
github.com/dxe/docs.

## Improving this document

For local development:

```
npm install
npm run start
```

To build the production site (do this before every commit):

```
npm run build
```

## How to deploy

```
git remote add dokku dokku@dxetech.org:docs
git push dokku master
```
