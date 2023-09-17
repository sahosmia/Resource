## Vue Router

```js
//router/index.js

import { createRouter, createWebHistory } from "vue-router";

import NotFound from "../pages/core/NotFound.vue";
import guestRoute from "../module/guest/router/guestRoutes";
import adminRoute from "../module/admin/router/adminRoutes";

const routes = [
  {
    path: "/register",
    name: "register",
    component: import("../pages/Register.vue"),
    meta: {
      title: "Register",
    },
  },
  {
    path: "/login",
    name: "login",
    component: import("../pages/Login.vue"),
    meta: {
      title: "Login",
    },
  },

  // Not Found
  {
    path: "/:pathMatch(.*)*",
    component: NotFound,
    meta: {
      title: "Not Found",
    },
  },

  ...guestRoute,
  ...adminRoute,
];

const router = createRouter({
  history: createWebHistory(),
  routes,
  linkActiveClass: "active-nav",
});

router.beforeEach((to, from, next) => {
  document.title = to.meta.title ? to.meta.title : "Travel Guid";
  next();
});

export default router;

```



```js
// App.vue

<template>
    <router-view></router-view>
</template>
```


```js
//use it in main.js
app.use(router)
```

















