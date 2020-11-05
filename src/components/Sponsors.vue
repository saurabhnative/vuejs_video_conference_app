<template>
  <div class="sponsors-container">
    <div class="text-left sponsors-title">
      Supportive sponsors
    </div>
    <div class="text-left sponsors-description">
      Thanking our sponsors
    </div>
    <div class="d-flex row sponsors-items-container">
      <div v-for="value in sponsors" v-bind:key="value" class="col-lg-4 col-12 sponsor-item">
        <div class="card sponsors-card d-flex align-items-center justify-content-center flex-row">
          <div>
            <i class="fa fa-money user-placeholder"></i>
          </div>
          <div>
            <span class="sponsor-item-title">{{ value }}</span>
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
  font-size: 4rem;
}
.sponsors-container {
  margin: 180px 40px;
}
@media only screen and (max-width: 600px) {
  .sponsors-container {
    margin: 20px 0px;
  }
  .sponsors-title { 
    font-size: 2rem !important;
  }
}
.sponsors-title {
  font-size: 2.25rem;
  font-weight: 600;
}
.sponsors-description {
  color: #aebdb5;
  font-size: 1.5rem;
}
.sponsors-items-container {
  margin: 30px 0px;
}
.sponsor-item {
  width: 100%;
  background: none;
}
.sponsors-card {
  background-color: rgba(156, 178, 199, 0.3);
  width: 100%;
  border-radius: 10px;
  height: 250px;
}
@media only screen and (max-width: 600px) {
  .sponsors-card {
    margin: 20px 0px;
  }
}
.sponsor-item-title {
  font-size: 2.5rem;
  font-weight: 600;
  margin-left: 10px;
}
</style>