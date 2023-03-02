<template>
  <h1 class="text-3xl text-[#42b983] pb-5">Events For Good</h1>

  <div class="flex justify-center">
    <div class="home space-y-4">
      <EventCard
        class="px-20 max-w-md"
        v-for="event in events"
        :key="event.id"
        :event="event"
      />
    </div>
  </div>
</template>

<script>
import EventCard from "@/components/EventCard.vue";

export default {
  name: "EventList",
  components: {
    EventCard,
  },

  data() {
    return {
      events: [
        {
          id: 1,
          category: "animal walfare",
          title: "Cat Adoption Day",
          description: "Find your new feline friend at this event",
          location: "Meow Town",
          date: "January 28, 2023",
          time: "12:00",
          petsallowed: true,
          organizer: "Ammar",
        },
        {
          id: 2,
          category: "sport",
          title: "Tennis Tournament",
          description:
            "Participate in this tournament to have a chance fight against Novak Djokovic",
          location: "Sport Town",
          date: "January 1, 2023",
          time: "12:00",
          petsallowed: true,
          organizer: "Ammar",
        },
        {
          id: 3,
          category: "food",
          title: "Community Gardening",
          description: "Join us to tend community edible plants 420",
          location: "Edibles Town",
          date: "February 10, 2023",
          time: "12:00",
          petsallowed: true,
          organizer: "Ammar",
        },
      ],
    };
  },
};
</script>
