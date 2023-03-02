<template>
  <div v-if="event">
    <h1 class="text-3xl font-semibold">{{ event.title }}</h1>
    <p class="p-4">
      {{ event.time }} on{{ event.date }} at {{ event.location }}
    </p>
    <p class="text-gray-800">{{ event.description }}</p>
  </div>
</template>

<script>
import axios from "axios";

export default {
  props: ["id"],
  data() {
    return {
      event: null,
    };
  },
  created() {
    //fetch event by id and set local data

    let url = `https://my-json-server.typicode.com/Code-Pop/Real-World_Vue-3/events/${this.id}`;
    axios
      .get(url)
      .then((response) => {
        this.event = response.data;
      })
      .catch((error) => {
        console.log(error);
      });
  },
};
</script>
