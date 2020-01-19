<template>
  <div class="calendar-header">
    <h2>{{currentYear}}년 {{currentMonth}}월</h2>
  </div>
</template>

<script>
export default {
  props: [
    'currentYear', 'currentMonth'
  ]
}
</script>

<style>

</style>