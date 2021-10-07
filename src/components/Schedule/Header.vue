<template>
  <header>
    <p>{{ title }}</p>
  </header>
</template>

<script>
export default {
  name: "Header",
  props: {
    title: {
      type: String,
      default: "Schedule",
    },
  },
};
</script>

<style scoped>
header {
  height: 50px;
  display: flex;
  align-items: center;
  justify-content: flex-start;
}
</style>