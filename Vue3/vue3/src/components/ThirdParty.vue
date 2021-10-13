<template>
  <div>
    <h1>ThirdParty.vue</h1>
    <div class="codes">
      <div class="code">
        <h3>Vue2</h3>
        <pre>
          <code>
{{`Vue.use(myPlugin);
new Vue({/* Vue 초기화 */});`}}
          </code>
        </pre>
      </div>
      <div class="code">
        <h3>Vue3</h3>
        <pre>
          <code>
{{`const app = createApp();
app.use(myPlugin);`}}
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
  name: "ThirdParty",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
