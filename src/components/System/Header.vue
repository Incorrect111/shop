<template>
  <header class="navbar">
      <div class="container">
        <div class="navbar-content">
          <router-link class="logo" to="/"> {{ title }} </router-link>
          <ul class="navbar-list">
            <li class="navbar-item" v-for="link in links" :key="link.title">
              <router-link
                class="navbar-link"
                :title="link.title"
                :to="link.url"
                >{{ link.title }}</router-link
              >
            </li>
          </ul>
        </div>
      </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      links: [
        { title: "Home", url: "/" },
        { title: "About", url: "/about" },
      ],
      title: 'Shop'
    };
  },
};
</script>

<style lang="scss">
.navbar-link {
  &.router-link-exact-active {
    color: rgb(134, 117, 228);
  }
}
</style>
