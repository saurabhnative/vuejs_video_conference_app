<template>
    <div class="events-container">
        <div class="info-title text-left">
            Enrich your frontend skills
        </div>
        <div class="info-description text-left">
            Loads of sessions on Vue.js development, testing and deployment
        </div>
        <div class="event-container d-flex text-left">
            <div>
                <img src="/assets/event.jpg" alt="event image" class="event-image"/>
            </div>
            <div class="event-container-text-section d-flex justify-content-center flex-column">
                <div class="info-eventName">
                Online Sessions
                </div>
                <div class="info-event-description">
                Learn from leading speakers who are experts in Vue.js development, Vuetify from India. 
                All of this from the comfort of yor home.
                Tickets also guarantee access to session recordings to listen to the talks later.
                </div>
                <div>
                    <button class="btn btn-danger action-button" type="button">
                        Register Now
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>

<style>
.events-container {
    margin: 100px 40px;
}
.info-title {
    font-size: 2.25rem;
    font-weight: 600;
}
.info-description {
    font-size: 1.5rem;
    color: #aebdd5;
}
.info-eventName {
    font-size: 1.8rem;
    font-weight: 600;
}
.info-event-description {
    font-size: 1.25rem;
    color: #aebdd5;
}
.event-container {
    margin: 50px 0px;
}
.event-container-text-section {
    padding: 0px 30px;
}
.event-image {
    border-radius: 10px;
    opacity: 0.5;
    height: 300px;
}
.action-button {
    width: 200px;
    height: 48px;
    border-radius: 30px;
    font-size: 1.2rem;
    font-weight: 700;
    margin-top: 30px;
}
</style>