<template>
  <section class="container">
    <div>
      <h1 class="title">
        nuxt-bug3
      </h1>
      <h2 class="subtitle">
        Nuxt.js project
      </h2>
      <div class="links">
        <nuxt-link class="button--green" to="/srchComponent">Go to srchComponent in the root, it has the bug</nuxt-link>
        <nuxt-link class="button--grey" to="/nuxtChildWrapper/srchComponent">Go to srchComponent wrapped in nuxt-child, there's no bug</nuxt-link>
      </div>
    </div>
  </section>
</template>

<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
