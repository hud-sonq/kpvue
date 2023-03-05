<template>
  <div ref="list" class="ticker">
    <div  v-for="item in items">
      <slot></slot>
    </div>
  </div>
</template>

<style>

body {
  overflow: hidden;
}

@keyframes slide {
  from {
    background-position-x: 0;
  } to {
    background-position-x: -100%;
  }
}

.ticker {
  width: 200%;
  text-align: center;
  background-color: red;
  height: 50px;
  display: flex;
  animation: 5s linear infinite slide;
}

.tickercolor {
  color: white;
}
</style>

<script setup>

const list = ref(null);
const items = ref([{ message: 'Foo' }, { message: 'Bar' }])

defineProps(['content'])

onMounted(() => {
  // here get the children of that list
  // use a query selector of div.ctx
  // set innerText to the value passed from prop content
  console.log(list.value);
  const info1 = list.value.querySelectorAll("div.ctx")
  for (const [k, v] of Object.entries(info1)) {
    v.innerText = items.value[k].message
  }
  console.log(info1)
})

</script>