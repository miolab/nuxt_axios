# Nuxt.js (Axios)

`Nuxt.js`のお試しで、__API非同期通信__ を実装します。

- 実行環境・バージョン

  ```bash
  create-nuxt-app v2.15.0
  ```

  ```bash
  $ node --version
  v12.16.1
  ```

  - [Axios](https://github.com/axios/axios)

  - [JSONPlaceholder](https://jsonplaceholder.typicode.com/)

    - プロトタイプREST APIとして、[`/users`](https://jsonplaceholder.typicode.com/users)を使用。

## 実装コード

- [`pages/index.vue`](https://github.com/miolab/nuxt_axios/blob/master/pages/index.vue)

## 結果表示

<img width="922" alt="get_api_result" src="https://user-images.githubusercontent.com/33124627/82008351-68317d00-96a7-11ea-848f-b486cb072f04.png">

- [localhost:3000](localhost:3000)

---

## Build Setup

```bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev
```

For detailed explanation on how things work, check out [Nuxt.js docs](https://nuxtjs.org).
