<template>
  <h1 class="text-3xl text-[#42b983] pb-5">Events For Good</h1>

  <div class="flex justify-center">
    <div class="home space-y-4">
      <EventCard
        class="px-20 max-w-4xl"
        v-for="event in events"
        :key="event.id"
        :event="event"
      />
    </div>
  </div>
</template>

<script>
import EventCard from "@/components/EventCard.vue";
import axios from "axios";

export default {
  name: "EventList",
  components: {
    EventCard,
  },

  data() {
    return {
      events: null,
    };
  },

  props: ["id"],

  created() {
    axios
      .get(
        "https://my-json-server.typicode.com/Code-Pop/Real-World_Vue-3/events"
      )
      .then((response) => {
        this.events = response.data;
      })
      .catch((error) => {
        console.log(error);
      });
  },
};
</script>
