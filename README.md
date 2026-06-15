# Secured-information-details-
gh repo create secureid-landing --public --source=. --remote=origin --push
name: Publish Package  on: [push]  jobs:   publish:     runs-on: ubuntu-latest     permissions:       packages: write       contents: read     steps:       - uses: actions/checkout@v3       - uses: actions/setup-node@v3         with:           node-version: '18'           registry-url: https://npm.pkg.github.com/       - run: npm publish         env:           NODE_AUTH_TOKEN: ${{ secrets.GITHUB_TOKEN }}~/.npmrc
.npmrc//npm.pkg.github.com/:_authToken=YOUR_TOKENexport NPM_TOKEN=YOUR_TOKEN
npm config set //npm.pkg.github.com/:_authToken=$NPM_TOKEN
