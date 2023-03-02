<template>
  <div
    class="event-card py-16 border-2 cursor-pointer hover:border-3 hover:border-[#42b983]"
  >
    <span class="">@ {{ event.date }}</span>
    <h4 class="text-2xl font-semibold">{{ event.title }}</h4>
  </div>
</template>

<script>
export default {
  name: "EventCard",
  props: {
    event: Object,
  },
};
</script>
