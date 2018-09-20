# truffle-analyze

Adds a patch on top of truffle for enabling the analyze command:
```
$ npm i -g truffle-analyze

$ mkdir test && cd $_

$ truffle-analyze init

[ write some contracts, build them ]

$ truffle-analyze analyze

```
This repo only contains the patches for truffle and the packaging. For the
patching system it uses [patch-package](https://github.com/ds300/patch-package).
For adding/updating a patch, from this cloned repo:
```
$ npm i

[ modify node_modules/truffle-core as needed ]

$ npx patch-package truffle-core

$ git add patches/*

$ git commit -m"new patch added..."
```
