
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
import Pomodoro from "vuemodoro";

export default {
  name: "App",
  data() {
    return {
      number: 0,
    };
  },
  components: {
    Pomodoro,
  },
  // rest of the component
};
</script>