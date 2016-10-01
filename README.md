# npm-quick-tutorial
NodeJs npm quick tutorial - in 5 minutes.

## Into
Npm official homepage: https://www.npmjs.com/

"npm is the package manager for JavaScript. Find, share, and reuse packages of code from hundreds of thousands of developers — and assemble them in powerful new ways." [npmjs.com]

Official getting started guide: https://docs.npmjs.com/getting-started/what-is-npm

## Most useful commands

`npm -v` gets your version of npm

`npm init` created basic package.json - interactive process

`npm install` (npm install / npm i) install dependencies from package.json / npm-shrinkwrap.json (if locked)

`npm install PACKAGE_NAME` installs new package (or change version with npm install somepackage@1.1.0)
* `-g` install globally
* `--save` saves package into dependenvies (package.json)
* `--save-dev`  saves package into development dependencies (package.json)

`npm update` (npm update --save / --save-dev) updates dependencies

`npm prune` removes unnecessary dependencies (not licted in packages.json)

`npm shrinkwrap` lock dependencies (npm install will be installing versions from npm-shrinkwrap.json file)

`npm start` starts application (start script entry must be defined in packages.json)

`npm test` run tests (tests script entry must be defined in packages.json)

`npm run CUSTOM_ENTRY_NAME` runs custom command defined in packages.json (scripts entry)

`npm dedupe` reduces dependencies duplication by moving deps up on the tree

`npm publish` publishes application into npmjs server

More commands in official documentation https://docs.npmjs.com/

## How to pass parameters inside scripts function

By passing params with `-`/`--` params are available only in declaration of command in package.json.

Example package.json:
```
...
"scripts": {
  "somescript": "npm run otherscript"
}
...
```

If we want to pass parameters into `otherscript` through `somescript` we would need to use command `--` before actual parameter:

* `npm run somescript -- --parameter=value`

With "double --" parameters are passed directly into nested function.
