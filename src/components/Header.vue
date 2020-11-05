<template>
  <nav class="navbar navbar-dark bg-dark header">
    <div class="text-light h1 mt-1">Vue.js India</div>
    <div class="ml-auto d-flex align-items-center right-section">
      <div class="btn btn-light mr-2"><b>Sponsors</b></div>
      <button class="btn btn-light mr-2 " type="button"><b>Speakers</b></button>
      <button class="btn btn-danger" type="button"><b>Register</b></button>
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
  padding-left: 0px;
}
@media only screen and (max-width: 600px) {
  .header {
    margin: 0px;
  }
  .right-section {
    margin-left: 0px !important;
  }
}
</style>