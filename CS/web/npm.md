## Package.json:

when more developers want to collaborate we can use this so others can get the exact dependencies which we are using

### Semantic versioning:

5.21.17

5 is Major

If it is major change

21 is minor

If it is feature and it supports the previous versions then update minor

17 is patch

If it is bug fix then update patch

5.21.17 exact version

Greater than > 5.21.17

Compatible version ^5.21.17 only the minor and patch versions will change

Minor level changes ~5.21.17 only the patch versions will change

Pre release versions

5.21.17-alpha

5.21.17-beta

### npm install

npm install package or npm i package

Will install package in dependencies section in package.json

npm install package –save-dev or npm install package -D

Will install package in development dependencies section in package.json

npm install package --production

Will not install packages from dev dependenciesc

npm install package@5.21.17

Install the specific package

Package-lock.json should be committed to git

Keeps track of the dependencies and its child dependencies

### npm update

Will update the versions

^5.21.17 to recent ^5.24.12

To run scripts in parallel

Npm install npm-run-all

'all' : 'npm-run-all –parallel start custom custom1'

Can also use serial flag instead of parallel

### shebang

/usr/bin/env node (on unix operating system to understand where the node is present)

### Browser app

Browser app will have an index.html file

Browser will have no effect whether u have added it as a dev dependency or dependency

### Server app

Server app will not have index.html file
