<template>
  <div id="app">
    <Header />
    <div v-if="shouldShowContent">
      <ConferenceVideo :isConferenceStarted="isConferenceStarted" />
      <div v-if="!isConferenceStarted" class="m-4">
        <button @click="isConferenceStarted = true" class="btn btn-primary">
          <span class="h3">Start Conference</span>
        </button>
      </div>
      <Speakers :speakers="speakers" />
      <Sponsors :sponsors="sponsors" />
    </div>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Speakers from "./components/Speakers.vue";
import Sponsors from "./components/Sponsors.vue";
import ConferenceVideo from "./components/ConferenceVideo.vue";
export default {
  name: "App",
  components: {
    Header,
    ConferenceVideo,
    Speakers,
    Sponsors,
  },
  data() {
    return {
      shouldShowContent: false,
      speakers: ["Speaker 1", "Speaker 2", "Speaker 3"],
      sponsors: ["Sponsor 1", "Sponsor 2"],
      isConferenceStarted: false,
    };
  },
  beforeCreate() {
    console.log("beforeCreate method");
    console.log("The status of available data is: ", this.speakers, this.sponsors);
  },
  created() {
    // console.log("created method");
    // console.log(
    //   "The status of available data is: ",
    //   this.speakers,
    //   this.sponsors
    // );
    // this.shouldShowContent = true;
  },
  beforeMount() {
    // console.log("Values of this.$el", this.$el);
  },
  mounted() {
    // Print value of dom element
    // console.log("Values of this.$el in mounted", this.$el);
  },
  beforeUpdate() {
    // console.log(
    //   "Value of isConferenceStarted in beforeUpdate(): ",
    //   this.isConferenceStarted
    // );
  },
  updated() {
    // console.log(
    //   "Value of isConferenceStarted in updated():",
    //   this.isConferenceStarted
    // );
  },
  beforeDestroy() {
    // this.isConferenceStarted = null;
    // delete this.isConferenceStarted;
  },
  destroyed() {
    // console.log("Send analytics ");
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
