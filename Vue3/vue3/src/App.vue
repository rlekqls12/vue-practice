<template>
  <div>
    <p>Count: {{ count }} (Press '+' Key)</p>
    <p>Multiply Count: {{ multiplyCount }}</p>
    <hr />
    <Filter />
    <ModelSync />
    <ThirdParty />
    <CompositionApi />
  </div>
</template>

<script>
import { computed, onMounted, onUnmounted, ref, watch } from "vue";
import Filter from "./components/Filter.vue";
import ModelSync from "./components/ModelSync.vue";
import ThirdParty from "./components/ThirdParty.vue";
import CompositionApi from "./components/CompositionApi.vue";

// Hook
function useCounter() {
  const counter = ref(0);
  const increment = () => counter.value++;
  return {
    counter,
    increment,
  };
}

export default {
  name: "App",
  components: {
    Filter,
    ModelSync,
    ThirdParty,
    CompositionApi,
  },
  setup() {
    const { counter: count, increment: incrementCount } = useCounter();
    // const data = reactive({
    //   count: 0,
    // });

    // const incrementCount = () => data.count++;
    const onKeydownPlus = (e) => e?.keyCode === 187 && incrementCount();
    const multiplyCount = computed(() => count.value * 2);

    watch(count, (val) => console.log("count", val));

    onMounted(() => {
      document.addEventListener("keydown", onKeydownPlus);
    });
    onUnmounted(() => {
      document.removeEventListener("keydown", onKeydownPlus);
    });

    return {
      // ...toRefs(data),
      count,
      multiplyCount,
    };
  },
};
</script>

<style>
* {
  margin: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  padding: 20px;
}

.codes {
  display: flex;
}
.code {
  border: 1px solid black;
  padding: 5px;
}
</style>
