<h1 align="center">conventional-changelog-yl</h1>
<p>
  <img src="https://img.shields.io/badge/version-0.1.0-blue.svg?cacheSeconds=2592000" />
  <a href="https://github.com/ITxiaohao/conventional-changelog-custom-config#readme">
    <img alt="Documentation" src="https://img.shields.io/badge/documentation-yes-brightgreen.svg" target="_blank" />
  </a>
  <a href="https://github.com/ITxiaohao/conventional-changelog-custom-config/blob/master/LICENSE">
    <img alt="License: MIT" src="https://img.shields.io/badge/License-MIT-yellow.svg" target="_blank" />
  </a>
</p>

> This preset extends the [conventional-changelog-angular](https://github.com/conventional-changelog/conventional-changelog/blob/master/packages/conventional-changelog-angular/README.md) preset

前置插件准备

- 使用 standard version 自动发布版本生成CHANGELOG


```sh
npm install standard-version conventional-changelog-yl --save-dev
```

## Configuration

在 package.json 中配置参数

### 不填配置的话则会按照 angular 的预设模版生成 CHANGELOG

```json
{
  "scripts": {
    "release": "standard-version --preset yl"
  },
  "repository": {
    "url": "**repoUrl**"
  },
  "changelog": {
    "emojis": false
  }
}
```

**bugsUrl**

Type: `string` Default: `true`

默认`bugsUrl: 'http://team.yongliweb.cn/zentao/bug-view-'`

如果不填 `bugsUrl` 则会根据 **package.json** 中的 `repository.url` 来作为 issues URL

**emojis**

Type: `boolean` Default: `true`

### emojis types 参考 [gitmoji](https://gitmoji.carloscuesta.me/)

| Commit Type | Title                    | Description                                                                                                 | Emojis |
| ----------- | ------------------------ | ----------------------------------------------------------------------------------------------------------- | ------ |
| `feat`      | Features                 | A new feature                                                                                               | ✨     |
| `fix`       | Bug Fixes                | A bug Fix                                                                                                   | 🐛     |
| `docs`      | Documentation            | Documentation only changes                                                                                  | 📝     |
| `style`     | Styles                   | Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)      | 💄     |
| `refactor`  | Code Refactoring         | A code change that neither fixes a bug nor adds a feature                                                   | ♻️     |
| `confict`   | Conficts                 | Resolve Conflicts                                                                                           | ⚡️     |
| `test`      | Tests                    | Adding missing tests or correcting existing tests                                                           | ✅     |
| `build`     | Build                    | Changes that affect the build system or external dependencies (example scopes: gulp, broccoli, npm)         | 👷     |
| `ci`        | Continuous Integrations  | Changes to our CI configuration files and scripts (example scopes: Travis, Circle, BrowserStack, SauceLabs) | 🔧     |
| `chore`     | Chores                   | Other changes that don't modify src or test files                                                           | 🎫     |
| `revert`    | Reverts                  | Reverts a previous commit                                                                                   | ⏪     |

**authorName**

Type: `boolean` Default: `true`

在 CHANGELOG 中生成用户名

**authorEmail**

Type: `boolean` Default: `false`

在 CHANGELOG 中生成邮箱

## Usage

需要发布版本时，运行以下命令，将会自动打tag并且更新Changelog并commit

```sh
npm run release
```
