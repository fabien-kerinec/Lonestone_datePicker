<template>
  <div class="hours">
    <div class="head">
      <p>Time</p>
      <Time hours="10" minutes="10" morning="true" />
    </div>
    <div class="content">
      <ul>
        <li v-for="n in 24" :key="n">
          <Time :hours="n" minutes="00" :morning="n < 12 ? true : false" />
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import Time from "./Time.vue";

export default {
  name: "Hours",
  components: {
    Time,
  },
};
</script>

<style scoped>
.hours {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
}
.head {
  display: flex;
  align-items: center;
  margin-bottom: 15px;
}
p {
  margin-right: 10px;
}
ul {
  height: 400px;
  overflow: auto;
  margin: 0;
  padding: 0;
}
li {
  list-style: none;
  padding: 0;
  margin: 0;
  margin: 5px 0;
}
</style>