<template>
  <nav class="navbar navbar-dark bg-dark header">
    <div class="text-light h1">Vue.js India</div>
    <div class="ml-auto d-flex align-items-center">
      <div class="btn btn-light mr-2"><b>Sponsors</b></div>
      <button class="btn btn-light mr-2 " type="button"><b>Speakers</b></button>
      <button class="btn btn-danger" type="button">Register</button>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style>
.header {
  margin: 0px 40px;
}
</style>