# cypress-first-time

## インストール

- `npm i cypress`
- All in one なので、これだけで良いらしい
- Cypress の Assertion は微妙なので、後で Karma や Mocha を入れたくなるらしい

## IDE 起動

- `npx cypress open`
- 勝手に`cypress`ディレクトリを作ってくれる
  ![cypress_ide](./img/cypress_ide.png)

## Cypress でテストを書いてみる

- `touch cypress/integration/google_spec.js`
- integration 内に js ファイルを作成
- [google_spec.js](./cypress/integration/google_spec.js)に Google のトップページにアクセスすると、タイトルに Google と表示されているというテストを記述する

## [Cypress ESLint Plugin](https://github.com/cypress-io/eslint-plugin-cypress)を導入

- `npm install eslint-plugin-cypress --save-dev`
- [.eslintrc.json](./.eslintrc.json)に以下を追加
- テストファイルが真っ赤になるのを防止

```json
  "extends": [
    "plugin:cypress/recommended"
  ],
  "plugins": [
    "cypress"
  ],
```

## テスト実行
* IDEからファイル名をクリックする
* Chromeが開いてテストが実行される
![cypress_run](./img/cypress_run.png)

## 参考

- <https://qiita.com/okitan/items/b44882e28006c1be32b7>
