<template>
  <div class="m-2" v-if="isConferenceStarted">
    <video width="800" controls ref="video">
      <source src="/assets/video.mp4" type="video/mp4" />
    </video>
    <div>
      Video Courtesy: Bedrijfsfilmspecialist.nl from Pexels
    </div>
  </div>
</template>

<script>
export default {
  name: "ConferenceVideo",
  props: {
    isConferenceStarted: Boolean,
  },
  created() {
    // console.log(this.isConferenceStarted);
  }
};
</script>