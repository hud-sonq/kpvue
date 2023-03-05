
<template>
  <div id="app">
    <b-field class="timer">
      <!-- <b-numberinput v-model="number"></b-numberinput> -->
      <input v-model="number" type="number" placeholder="Timer duration" />
    </b-field>
    <Pomodoro :key="number" :minutes="number" />
  </div>
</template>

<script>
</script>