<template>
  <div class="calendar-day">
    <strong class="tit-day">{{dayOfMonth}}</strong>
  </div>
</template>

<script>
export default {
  props: [
    'dayOfMonth'
  ],
  data() {
    return {

    }
  }
}
</script>

<style>
.calendar-day {
  position: relative;
}
.today {
  background-color: beige;
}

</style>