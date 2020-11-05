<template>
  <div class="container text-left event-container">
      <div class="event-date">6-8th December 2020</div>
      <div class="event-title">Vue.js India</div>
      <div class="event-description">
          Join 2,000+ Vue.js developers from India for a two-day conference to learn and discuss about the latest happenings of Vue.js and related technologies.
      </div>
      <div class="d-flex buttons-container">
          <button class="btn btn-danger action-button" type="button">
              Register Now
          </button>
          <button class="btn btn-light action-button ml-4" type="button" @click="startConference">
              Start Conference
          </button>
      </div>
  </div>
</template>

<script>
export default {
  name: "ConferenceVideo",
  props: ['startConference']
};
</script>

<style scoped>
.event-container {
    margin: 190px 40px;
}
@media only screen and (max-width: 600px) {
  .event-container {
    margin: 40px 0px;
  }
}
.event-date {
    color: #75c05e;
    font-size: 1.5rem;
    font-weight: 600;
}
.event-title {
    font-size: 4rem;
    color: white;
    font-weight:700;
}
.event-description {
    color: #aebdb5;
    font-size: 1.5rem;
}
.buttons-container {
    margin: 20px 0px;
}
.action-button {
    width: 200px;
    height: 48px;
    border-radius: 30px;
    font-size: 1.2rem;
    font-weight: 700;
}
@media only screen and (max-width: 600px) {
  .action-button {
    width: 150px;
    font-size: 1rem;
  }
}
</style>
