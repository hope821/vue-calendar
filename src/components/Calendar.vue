<template>
  <div class="jh-wrap">
    <h1>Calendar</h1>
    <main>
      <CalendarHeader
        :currentYear="currentYear"
        :currentMonth="currentMonth"
      ></CalendarHeader>
      <CalendarMonth
        :class="'month-type' + monthType"
        :currentYear="currentYear"
        :currentMonth="currentMonth"
        :currentDay="currentDay"
      ></CalendarMonth>
      <p :class="'month-type'+monthType">{{today}}</p>
    </main>
  </div>
</template>

<script>
import CalendarMonth from './CalendarMonth'
import CalendarHeader from './CalendarHeader'

export default {
  components: {
    CalendarMonth, CalendarHeader
  },
  data() {
    return {
      today: new Date(),
      currentYear: new Date().getFullYear(),
      currentMonth: new Date().getMonth()+1,
      currentDay: new Date().getDate(),
      monthType: new Date(new Date().getFullYear(), new Date().getMonth(), 1).getDay()
    }
  }
}
</script>

<style>

</style>