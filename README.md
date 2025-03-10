# awesome-javascript
👨‍💻 let's simply set up JavaScript development environment
asdfasdf
## Tutorial
* [간단하게 구축해 보는 JavaScript 개발 환경](https://d2.naver.com/helloworld/2564557)ddddddd
* [Tutorial Repository](https://github.com/stunstunstun/awesome-javascript)
aaa
## Getting Started

### Prerequisites

| Required                             | Description                                                               |
| ------------------------------------ | ------------------------------------------------------------------------- |
| [Git](https://git-scm.com/)          | We follow the [GitHub Flow](https://guides.github.com/introduction/flow/) |
| [Node.js](nodejs.org)                | 10.16.0 LTS                                                               |
| [Yarn](https://yarnpkg.com/lang/en/) | 1.16.0 or above                                                           |

### Install Node, Yarn

The project manages the version of node through `nvm`.

```
$ curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.8/install.sh | bash
$ command -v nvm
$ nvm install 10.16.0
$ which node
$ npm install -g yarn
```

In the project root as follows are performed through the `.nvmrc`

```
$ nvm use
...
```

## Yarn CLIs

### Install project

```bash
$ nvm use
$ yarn install
```

### Test

```bash
$ yarn test
```

## Create Git Repository
### Command
```
$ mkdir awesome-javascript
$ cd awesome-javascript
$ git init
...
$ git remote add origin https://github.com/${github_id}/awesome-javascript
$ git remote -v
origin  https://github.com/${github_id}/awesome-javascript (fetch)  
origin  https://github.com/${github_id}/awesome-javascript (push) 
```
### Link
* [Git](https://git-scm.com/)
* [GitHub](https://github.com/)
* [Pro Git](https://git-scm.com/book/ko/v2)
* [GitHub Help](https://help.github.com/en)

## Github Template for Issue & Pull Request
### Command
```
$ git checkout -b devops/github-templates
$ mkdir .github
$ touch .github/PULL_REQUEST_TEMPLATE.md # Create pull request template
$ cd .github
$ mkdir ISSUE_TEMPLATE
$ touch .github/bug_report.md # Create bug report template
$ touch .github/feature_request.md # Create feature request template
$ git commit -m 'chore: create issue & pull request template'
$ git push -u origin devops/github-templates
```

### Link
* [Manually creating a single issue template for your repository](https://help.github.com/en/articles/manually-creating-a-single-issue-template-for-your-repository)
* [Creating a pull request template for your repository](https://help.github.com/en/articles/creating-a-pull-request-template-for-your-repository)

## Node.js, npm and Yarn
### Command
```
$ curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.8/install.sh | bash
$ nvm install 10.15.3
$ node -v && npm -v
v10.15.3  
6.4.1
$ npm install yarn -g
```
### Link
* [Node.js](https://nodejs.org/ko/docs)
* [npm](https://docs.npmjs.com)
* [Yarn](https://yarnpkg.com/en/docs)

## Create Project
### Command
```
$ yarn init
yarn init v1.6.0
question name (awesome-javascript):
question version (1.0.0):
...
success Saved package.json
Done in 5.97s.
```
**package.json**
```
{
  "name": "awesome-javascript",
  "version": "1.0.0",
  "main": "index.js",
  "repository": "https://github.com/dl0312/awesome-javascript",
  "author": "Geon Lee <leegun2003@gmail.com>",
  "license": "MIT"
}
```
add `node-fetch` module with `yarn add node-fetch` for HTTP request
```
$ yarn add node-fetch
```
**package.json**
```
{
  ...
  "license": "MIT",
  "dependencies": {
    "node-fetch": "^2.6.0"
  }
}
```
**yarn.lock**
```
# THIS IS AN AUTOGENERATED FILE. DO NOT EDIT THIS FILE DIRECTLY.
# yarn lockfile v1


node-fetch@^2.6.0:
  version "2.6.0"
  resolved "https://registry.yarnpkg.com/node-fetch/-/node-fetch-2.6.0.tgz#e633456386d4aa55863f676a7ab0daa8fdecb0fd"

```
### SemVer(Semantic Versioning)
1. `MAJOR version` when you make incompatible API changes,
2. `MINOR version` when you add functionality in a backwards-compatible manner, and
3. `PATCH version` when you make backwards-compatible bug fixes.

### Link
* [Semantic Versioning](https://semver.org/)
* [npm package.json에서 틸드(~) 대신 캐럿(^) 사용하기](https://blog.outsider.ne.kr/1041)
* [npm-package.json](https://docs.npmjs.com/files/package.json#dependencies)
* [yarn.lock](https://yarnpkg.com/lang/en/docs/yarn-lock/)

## Share Project
### Command
```
$ echo "node_modules/" > .gitignore
$ git add .
$ git checkout -b issue/1
$ git commit -m 'Create project with Yarn'
$ git push -u origin issue/1
```
### Link
* [.gitignore](https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository#_ignoring)
* [The example of pull request](https://github.com/stunstunstun/awesome-javascript/pull/2)

## README.md
### Link
* [The example of README.md](https://github.com/stunstunstun/awesome-javascript/blob/master/README.md)

## Setting Test Environment with Jest
### Create Test Code
```
$ mkdir __tests__ lib
$ touch __tests__/github.test.js
$ touch lib/github.js
$ yarn test
```

### Link
* [GitHub REST API v3](https://developer.github.com/v3/)
* [Jest](https://jestjs.io/)
* [Jest-Getting Started](https://jestjs.io/docs/en/getting-started)

## Automate testing with Travis CI
### Delegated tasks for Travis CI
* Verification of [Code Convention](https://google.github.io/styleguide/jsguide.html) with [ESLint](https://eslint.org/)
* Automate testing with best practices
### Link
* [Jenkins](https://jenkins.io/)
* [Travis CI](https://travis-ci.org/)
* [Travis CI Tutorial](https://docs.travis-ci.com/user/tutorial/)
* [Code Convention](https://google.github.io/styleguide/jsguide.html)
* [ESLint](https://eslint.org/)
