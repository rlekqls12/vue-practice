<template>
  <div>
    <h1>Filter.vue</h1>
    <h3>filter 옵션에서 methods 옵션으로 이동</h3>
    <div class="codes">
      <div class="code">
        <h3>Vue2 Filter</h3>
        <pre>
          <code>
{{`{ price | toCurrency }`}}
          </code>
        </pre>
      </div>
      <div class="code">
        <h3>Vue3 Methods</h3>
        <pre>
          <code>
{{`{ toCurrency(price) }`}}
          </code>
        </pre>
      </div>
    </div>
    <br />
    <hr />
    <br />
  </div>
</template>

<script>
export default {
  name: "Filter",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
