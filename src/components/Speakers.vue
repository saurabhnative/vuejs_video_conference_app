<template>
  <div class="speakers-container">
    <div class="w-100 text-left speakers-text">Speakers</div>
    <div class="text-left speakers-description">
      Meet our incredible speakers from different regions of India!
    </div>
    <div class="d-flex row my-4">
      <div v-for="value in speakers" v-bind:key="value" class="col-lg-3 col-12">
        <div class="card d-flex align-items-center speaker-card justify-content-center">
          <i class="fa fa-user-circle user-placeholder"></i>
          <div class="card-body">
            <h5 class="card-title speaker-name">{{ value }}</h5>
            <p
              class="card-text"
            >Speaker Information</p>
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
.speakers-text {
  font-size: 2rem;
  font-weight: 600;
}
.speakers-description {
  font-size: 1.5rem;
  color: #aebdb5;
}
.card {
  background: none;
  border:none;
}
.speaker-card {
  background-color: rgba(156, 178, 199, 0.3);
  width: 100%;
  border-radius: 10px;
  height: 370px;
}
.card-body {
  flex: none;
}
.user-placeholder {
  font-size: 10rem;
  margin-top: 10px;
}
.speakers-container {
  margin: 20px 40px;
}
.speaker-name {
  font-size: 1.25rem;
  font-weight: 600;
  color: #4db879;
}
</style>