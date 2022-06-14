<template>
  <div class="fixed-navbar">
    <b-navbar toggleable="lg" type="dark" variant="info">
      <b-navbar-brand class="header-logo">
        <nuxt-link to="/">
          <div class="logo">
            <img src="@/assets/images/Vale Side Logo.svg" alt="logo" width="200px" height="50px"/>
          </div>
        </nuxt-link>
      </b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav class="ml-auto">
          <b-nav-item href="/">Home</b-nav-item>
          <b-nav-item href="/AboutUs">About Us</b-nav-item>
          <b-nav-item href="/OurServices">Services</b-nav-item>
          <b-nav-item href="/OurContact">Contact Us</b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {}
</script>

<style>
.b-nav-item {
  align-content: right;
}
.logo {
  width: 200px;
  height: 50px;
}
</style>