<template>


    <section class="events">

      <EventItem title="Event 1" content="Event 1 content"  type="quiz" date="2023-01-15" status="Active"/>
      <EventItem title="Event 2" content="Event 2 content" type="quiz" date="2022-12-03" status="Completed" />
      <EventItem title="Event 3" content="Event 3 content" type="quiz" date="2022-09-23" status="Completed" />

    </section>

</template>

<script>
import EventItem from "@/components/EventItem.vue";

export default {
  name: "Events",
  components: {EventItem}
}
</script>

<style scoped>
.events {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  margin: 10px;

}
</style>