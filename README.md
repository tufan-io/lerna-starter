# lerna-starter

This is an opinionated lerna mono-repo setup, to help get tufan-collections
setup.

## Opinions

Our opinions on how to [setup a lerna mono-repo](./docs/lerna-setup.md).

## Getting started

### Developing in the mono-repo

```bash
# 1. Clone the repo into the root of ypur desired mono-repo
git clone https://github.com/tufan-io/lerna-setup .

# 2. reconfigure the mono-repo. Asks a few questions to reconfigure
node ./.lerna-init

# 3. Install root module dependencies
npm install

# 4. Add sub-module: interactive prompts automate starter repo reinitialization.
npm add-sub-module

# 5. commiteszen is configured on the lerna mono-repo, so to commit changes
git cz

# From this point on, it's really a lerna mono-repo.
# equivalent npm commands are provided for your's truly, and anyone who has
# significant trouble with retraining muscle memory!

# 6. bootstrap the lerna sub-modules.
lerna bootstrap
npm run bootstrap

# 7a. If sub-modules are to be published to npm,
lerna publish
npm run publish

# 7b. If private git url based sub-modules are to be published,
lerna run git-publish
npm run git-publish

```

## License

This module is a container, and in principle, each sub-module should be consulted
for individual licensing declarations. To the extent that the boiler-plate settings of this module need a license, it's  [Apache-2.0](./APACHE-2.0.md)

## Code of Conduct

Please note that this project is released with a [Contributor Code of Conduct](code-of-conduct.md). By participating in this project you agree to abide by its terms.

## Support

Bugs, PRs, comments, suggestions welcomed!
