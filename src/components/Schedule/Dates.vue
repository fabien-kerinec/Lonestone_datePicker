<template>
  <div class="dates">
    <div class="head">
      <p>Date</p>
      <Day day="01" month="10" year="2021" />
    </div>
    <div class="content">
      <div class="month">
        <p>May 2021</p>
        <div class="arrows">
          <p>&#60;</p>
          <p>&#62;</p>
        </div>
      </div>
      <div class="day">
        <div class="top">
          <p class="unactive">S</p>
          <p class="unactive">M</p>
          <p class="unactive">T</p>
          <p class="unactive">W</p>
          <p class="unactive">T</p>
          <p class="unactive">F</p>
          <p class="unactive">S</p>
        </div>
        <div class="bottom">
          <ul>
            <li v-for="n in 31" :key="n">{{ n }}</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Day from "./Day.vue";

export default {
  name: "Dates",
  components: {
    Day,
  },
};
</script>

<style scoped>
.dates {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: flex-start;
}
.head {
  display: flex;
  align-items: center;
}
p {
  margin-right: 10px;
}
.content {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}
.month {
  width: 100%;
  display: flex;
  align-content: center;
  justify-content: space-between;

  margin-top: 15px;
  margin-bottom: 15px;
}
.arrows {
  display: flex;
}
.day {
  width: 100%;
  display: flex;
  flex-direction: column;
}
.top {
  width: 100%;
  display: flex;
  justify-content: space-between;
}
ul {
  padding: 0;
  margin: 0;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: center;
  width: 100%;
}
li {
  width: calc(100% / 7);
  display: flex;
  flex-wrap: wrap;
  list-style: none;
  padding: 0;
  margin: 0;
  margin: 10px 0;
}

p.unactive,
li.unactive {
  opacity: 0.7;
}
</style>