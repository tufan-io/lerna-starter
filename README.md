# lerna-starter

This is an opinionated lerna mono-repo setup, to help get tufan-collections
setup.

## Opinions

Our opinions on how to [setup a lerna mono-repo](./docs/lerna-setup.md).

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

## License

This module is a container, and in principle, each sub-module should be consulted
for individual licensing declarations. To the extent that the boiler-plate settings of this module need a license, it's  [Apache-2.0](./APACHE-2.0.md)

## Code of Conduct

Please note that this project is released with a [Contributor Code of Conduct](code-of-conduct.md). By participating in this project you agree to abide by its terms.

## Support

Bugs, PRs, comments, suggestions welcomed!
