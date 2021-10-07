<template>
  <p>{{ hours }}:{{ minutes }} {{ suffix }}</p>
</template>

<script>
import { computed } from "vue";
export default {
  name: "Time",
  props: {
    hours: {
      type: Number,
    },
    minutes: {
      type: Number,
    },
    morning: {
      type: Boolean,
    },
  },
  setup(props) {
    const suffix = computed(() => {
      return props.morning ? "AM" : "PM";
    });

    return { suffix };
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