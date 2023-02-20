<script>
export default {
  data() {
    return {
      dayWeek: "task1",
      dayWeekOptions: [
        "Monday",
        "Tuesday",
        "Wednesday",
        "Thursday",
        "Friday",
        "Saturday",
        "Sunday",
      ],
      dayYear: "",
      dayYearOptions: [
        1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20,
        21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31,
      ],
      monthYear: "",
      monthYearOptions: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12],
      yearYear: "",
      yearYearOptions: [
        2023, 2022, 2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014, 2013, 2012,
        2011, 2010, 2009, 2008, 2007, 2006, 2005, 2004, 2003, 2002, 2001, 2000,
      ],
    };
  },
  methods: {
    todayDate: function () {
      var today = new Date();
      this.dayYear = String(today.getDate());
      this.monthYear = String(today.getMonth() + 1);
      this.yearYear = today.getFullYear();
    },
  },
};
</script>
<template>
  <select v-model="dayWeek">
    <option v-for="option in dayWeekOptions">{{ option }}</option>
  </select>
  &nbsp;
  {{ dayWeek }}
  &nbsp;

  <select v-model="dayYear">
    <option v-for="option in dayYearOptions">{{ option }}</option>
  </select>
  <select v-model="monthYear">
    <option v-for="option in monthYearOptions">{{ option }}</option>
  </select>
  <select v-model="yearYear">
    <option v-for="option in yearYearOptions">{{ option }}</option>
  </select>
  <button class="button" @click="todayDate">Today's date</button>
</template>
<style>
.button {
    background-color: #293133; 
    border-radius: 8px;
    border: none;
    color: rgb(255, 255, 255);
    padding: 10px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 15px;
    margin: 4px 2px;
    cursor: pointer;
    -webkit-transition-duration: 0.4s; 
    transition-duration: 0.4s;
}
</style>