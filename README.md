# lerna-starter

This is an opinionated lerna mono-repo setup, to help get tufan-collections
setup. Find more details in [lerna setup](./lerna-setup.md).

## Getting started

### Developing in the mono-repo

```bash
# 1. Clone the repo into the root of ypur desired mono-repo
git clone https://github.com/sramam/lerna-setup .

# 2. Install root module dependencies
npm install

# 3. Add any desired sub-modules to ./sub-modules.
# if lerna is installed globally
lerna bootstrap

# if lerna is installed only as a local dependency
npx lerna bootstrap

```

### Publishing sub-modules

When the sub-modules are ready to be published, there are two options:

- npm hosting of sub-modules - typically public, but possibly private.

```bash
lerna publish
```

- git hosting of sub-modules - typically for development, possibly private.

```bash
lerna run gitpkg-publish
```

