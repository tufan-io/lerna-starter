# lerna settings

This is an opinionated starter repo for a lerna mono-repo. Specifically,

1. uses `sub-modules` as the home for contained modules. This is done to help with tab-completion when accessing the module directories via the CLI. `packages` requires an extra key-stroke - 's'. Call us lazy, we think it's better UX. It also sets this up as a yarn workspace, though, we prefer to stick with using npm.

2. uses an opinionated lerna config - specifically,
   - _enables hoisting._ This allows collating all sub-modules dependencies for a faster install. Importantly, `lerna bootstrap` also warns of version differences, making it easier to ensure all sub-modules are on the same version of a library.
   - _enables git-version._ Enables using private modules from git-repos.
   - makes explicit some other controls, like parallelism.

3. uses [git-mods](https://github.com/sramam/gitmods) coupled with [husky](https://github.com/typicode/husky) to ensure no unstaged/staged changes exist when committing or pushing respectively to the git repo. This is done to support a pattern in which we commit transpiled JavaScript into the main repo.

These are our opinions, hopefully you'll find them useful. YMMV.
