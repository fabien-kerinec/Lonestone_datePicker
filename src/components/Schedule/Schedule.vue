<template>
  <div class="schedule">
    <Header title="Schedule response" />
    <Calendar />
  </div>
</template>

<script>
import Header from "./Header.vue";
import Calendar from "./Calendar.vue";

export default {
  name: "Schedule",
  components: {
    Header,
    Calendar,
  },
};
</script>

<style>
.schedule {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  width: 500px;
  height: 500px;
  background: #f5f5f5;
  border-radius: 20px;
  padding: 20px;
  box-shadow: 0 0 10px 2px rgba(0, 0, 0, 0.3);
}
</style>