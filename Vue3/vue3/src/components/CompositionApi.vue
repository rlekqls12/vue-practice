<template>
  <div>
    <h1>CompositionApi.vue</h1>
    <div class="codes">
      <div class="code">
        <h3>Vue2 Extend</h3>
        <pre>
          <code>
{{`import Vue from 'vue';

export default Vue.extend({
  name: 'component-name',
  /* props, data, methods, ... */
});`}}
          </code>
        </pre>
      </div>
      <div class="code">
        <h3>Vue2 Composition Api</h3>
        <pre>
          <code>
{{`import { defineComponent } from '@vue/composition-api';

export default defineComponent({
  name: 'component-name',
  /* your component props, data, methods, etc. */  
});`}}
          </code>
        </pre>
      </div>
      <div class="code">
        <h3>Vue3 Composition Api</h3>
        <pre>
          <code>
{{`import { defineComponent } from '@vue/composition-api';

export default defineComponent({
  name: 'component-name',
  setup (props) {
    /* props, data, methods, ... */  
  }
});`}}
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
  name: "CompositionApi",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
