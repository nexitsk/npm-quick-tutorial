# npm-quick-tutorial
NodeJs npm quick tutorial - in 5 minutes.

## Into
Npm official homepage: https://www.npmjs.com/

"npm is the package manager for JavaScript. Find, share, and reuse packages of code from hundreds of thousands of developers — and assemble them in powerful new ways." [npmjs.com]

## Most useful commands

`npm -v` gets your version of npm

`npm install` (npm install / npm i) install dependencies from package.json / npm-shrinkwrap.json (if locked)

`npm update` (npm update --save / --save-dev) updated dependencies

`npm prune` removes unnecessary dependencies (not licted in packages.json)

`npm shrinkwrap` lock dependencies (npm install will be installing versions from npm-shrinkwrap.json file)

`npm start` starts application (start script entry must be defined in packages.json)

`npm test` run tests (tests script entry must be defined in packages.json)

`npm run CUSTOM_ENTRY_NAME` runs custom command defined in packages.json (scripts entry)

`npm dedupe` reduces dependencies duplication by moving deps up on the tree

`npm publish` publishes application into npmjs server

More commands in official documentation https://docs.npmjs.com/
