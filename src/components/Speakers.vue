<template>
  <div>
    <div class="w-100 text-center h3">Speakers</div>
    <div class="d-flex row m-4">
      <div v-for="value in speakers" v-bind:key="value" class="col-lg-4 col-12">
        <div class="card" >
          <i class="fa fa-user-circle user-placeholder"></i>
          <div class="card-body">
            <h5 class="card-title">{{ value }}</h5>
            <p
              class="card-text"
            >Speaker Information</p>
            <a href="#" class="btn btn-primary">Learn More</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Speakers",
  props: {
    speakers: Array,
  },
  created() {
    // console.log(this.speakers);
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