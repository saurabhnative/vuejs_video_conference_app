<template>
  <div id="app">
    <Header />
    <div v-if="shouldShowContent" class="content-container">
      <ConferenceInfo :startConference="startConference"/>
      <ConferenceVideo :isConferenceStarted="isConferenceStarted" />
      <Speakers :speakers="speakers" />
      <ConferenceEvents/>
      <Sponsors :sponsors="sponsors" />
    </div>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Speakers from "./components/Speakers.vue";
import Sponsors from "./components/Sponsors.vue";
import ConferenceVideo from "./components/ConferenceVideo.vue";
import ConferenceInfo from "./components/ConferenceInfo.vue";
import ConferenceEvents from "./components/ConferenceEvents";
export default {
  name: "App",
  components: {
    Header,
    ConferenceInfo,
    ConferenceVideo,
    Speakers,
    Sponsors,
    ConferenceEvents
  },
  data() {
    return {
      shouldShowContent: false,
      speakers: ["Speaker 1", "Speaker 2", "Speaker 3", "Speaker 4"],
      sponsors: ["Sponsor 1", "Sponsor 2", "Sponsor 3"],
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
    this.shouldShowContent = true;
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
  methods: { 
    startConference: function () {
        this.isConferenceStarted = !this.isConferenceStarted
    }
  }
};
</script>

<style>
body {
  background-color: #343a40;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: white;
  background-color: #343a40;
}
</style>
