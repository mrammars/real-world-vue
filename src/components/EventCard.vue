<template>
  <router-link :to="{ name: 'EventDetails', params: { id: event.id } }">
    <div
      class="event-card px-20 py-16 border-2 cursor-pointer hover:border-3 hover:border-[#42b983]"
    >
      <span class="">@ {{ event.date }}</span>
      <h4 class="text-2xl font-semibold">{{ event.title }}</h4>
    </div>
  </router-link>
</template>

<script>
export default {
  name: "EventCard",
  props: {
    event: Object,
  },
};
</script>
