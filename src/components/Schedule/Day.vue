<template>
  <p>{{ day }}/{{ month }}/{{ year }}</p>
</template>

<script>
export default {
  name: "Day",
  props: {
    day: {
      type: Number,
    },
    month: {
      type: Number,
    },
    year: {
      type: Boolean,
    },
  },
};
</script>

<style scoped>
p {
  text-transform: uppercase;
  padding: 5px 20px;
  border: 1px solid transparent;
  background: #e3e3e3;
  border-radius: 10px;
}
p.active {
  border: 1px solid #a6a6ed;
}
</style>