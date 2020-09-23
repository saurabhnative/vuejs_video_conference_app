<template>
  <div>
    <div class="w-100 text-center h3">Our awesome sponsors</div>
    <div class="d-flex row m-4">
      <div v-for="value in sponsors" v-bind:key="value" class="col-lg-4 col-12">
        <div class="card" >
          <i class="fa fa-money user-placeholder"></i>
          <div class="card-body">
            <h5 class="card-title">{{ value }}</h5>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Sponsors",
  props: {
    sponsors: Array,
  },
  created() {
    // console.log(this.sponsors);
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.user-placeholder {
  font-size: 10rem;
  margin-top: 10px;
}
</style>