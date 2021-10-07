<template>
  <section class="calendar">
    <Dates />
    <Hours />
  </section>
</template>

<script>
import Dates from "./Dates.vue";
import Hours from "./Hours.vue";

export default {
  name: "Calendar",
  components: {
    Dates,
    Hours,
  },
};
</script>

<style>
.calendar {
  width: 100%;
  display: flex;
  margin-top: 25px;
  /* justify-content: space-between; */
}
.dates,
.hours {
  flex: 0.6;
  display: flex;
  justify-content: flex-start;
  align-items: center;
}
.hours {
  flex: 0.4;
  justify-content: flex-end;
}
</style>