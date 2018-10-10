# Install npm:

### Curl
```
$ sudo apt install curl
```
### PPA
```
$ curl -sL https://deb.nodesource.com/setup_10.x | sudo bash -
```
### Install Node.js and NPM
```
$ sudo apt-get install -y nodejs
```
### Test
```
$ node -v
v10.11.0
$ npm -v
6.4.1
```
### Angular/cli
```
npm install -g angular-cli
```
### Alias to Zsh
Editing `~/.zshrc` with gedit or nano
```
alias ng="~/.npm-global/lib/node_modules/@angular/cli/bin/ng"
```

### Other link issues:
  - https://github.com/angular/angular-cli/issues/503
  - https://www.npmjs.com/package/@angular/cli#updating-angular-cli
