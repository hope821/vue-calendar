<template>
  <div class="calender-month"> 
    <CalendarDay 
      v-for="index in new Date(currentYear, currentMonth, 0).getDate()"
      :class="{today : index === currentDay}"
      :dayOfMonth="index"
      :key="'y' + currentYear + 'm' + currentMonth + 'd' + index"
    ></CalendarDay>
  </div>
</template>

<script>
import CalendarDay from './CalendarDay'

export default {
  components: {
    CalendarDay
  },
  props: [
    'currentYear', 'currentMonth', 'currentDay'
  ],
  data() {
    return {

    }
  }
}
</script>

<style>
  .calender-month {
    display: grid;
    grid-template-columns: repeat(7, 1fr);
    grid-gap: 10px;
    grid-auto-rows: minmax(100px, auto);
  }
  .month-type1 .calendar-day:first-child {
    grid-column-start: 2;
  }
  .month-type2 .calendar-day:first-child {
    grid-column-start: 3;
  }
  .month-type3 .calendar-day:first-child {
    grid-column-start: 4;
  }
  .month-type4 .calendar-day:first-child {
    grid-column-start: 5;
  }
  .month-type5 .calendar-day:first-child {
    grid-column-start: 6;
  }
  .month-type6 .calendar-day:first-child {
    grid-column-start: 7;
  }
</style>