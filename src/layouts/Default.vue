<template>
  <div class="container-layout">
    <div>
      <b-navbar centered="true" type="is-primary" class="navbar">
        <template #start>
          <b-navbar-item tag="router-link" :to="{ path: '/' }">
            Home
          </b-navbar-item>

          <b-navbar-item tag="router-link" :to="{ path: '/hero/' }">
            Hero
          </b-navbar-item>
        </template>
      </b-navbar>
      <slot />
    </div>

    <div>
      <b-navbar class="navbar" type="is-dark">
        <template #end>
          <b-navbar-item>
            Contact
          </b-navbar-item>
          <b-navbar-item>
            Email
          </b-navbar-item>
        </template>
      </b-navbar>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.container-layout {
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.navbar {
  height: 50px;
}
</style>
