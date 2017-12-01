# Developing in the mono-repo

```bash
# 1. Clone the repo into the root of ypur desired mono-repo
git clone https://github.com/tufan-io/lerna-setup .

# 2. Install root module dependencies
npm install

# 3. Add sub-module: interactive prompts automate starter repo reinitialization.
npm add-sub-module

# 4. commiteszen is configured on the lerna mono-repo, so to commit changes
git cz

# From this point on, it's really a lerna mono-repo.
# equivalent npm commands are provided for your's truly, and anyone who has
# significant trouble with retraining muscle memory!

# 5. bootstrap the lerna sub-modules.
lerna bootstrap
npm run bootstrap

# 6a. If sub-modules are to be published to npm,
lerna publish
npm run publish

# 6b. If private git url based sub-modules are to be published,
lerna run git-publish
npm run git-publish

```
