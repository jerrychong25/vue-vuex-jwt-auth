# Vue.js JWT Authentication with Vuex and Vue Router

[![GitHub release](https://img.shields.io/github/release/jerrychong25/vue-vuex-jwt-auth.svg)](https://gitHub.com/jerrychong25/vue-vuex-jwt-auth/releases/)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-no-red.svg)](https://github.com/jerrychong25/vue-vuex-jwt-auth/graphs/commit-activity)
[![HitCount](http://hits.dwyl.com/jerrychong25/vue-vuex-jwt-auth.svg)](http://hits.dwyl.com/jerrychong25/vue-vuex-jwt-auth)

For more detail, please visit:
> [Vue.js JWT Authentication with Vuex and Vue Router](https://bezkoder.com/jwt-vue-vuex-authentication/)

## Note:
Open `src/services/auth-header.js` and modify `return` statement for appropriate back-end.

```js
export default function authHeader() {
  let user = JSON.parse(localStorage.getItem('user'));

  if (user && user.accessToken) {
    return { Authorization: 'Bearer ' + user.accessToken }; // for Spring Boot back-end
    // return { 'x-access-token': user.accessToken };       // for Node.js Express back-end
  } else {
    return {};
  }
}
```

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Run your tests
```
npm run test
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
