<template>
  <div>
    <h1>ModelSync.vue</h1>
    <div class="codes">
      <div class="code">
        <h3>Vue2 Before</h3>
        <pre>
          <code>
{{`// 부모 component
&lt;child-component v-model="visible"/> \n

// 자식 component의 model 옵션
&lt;script&gt;
{
  model: {
    prop: 'visible',
    event: 'change'
  }
}
&lt;/script&gt;`}}
          </code>
        </pre>
      </div>
      <div class="code">
        <h3>Vue2 After</h3>
        <pre>
          <code>
{{`// 부모 component
&lt;child-component v-bind:visible.sync="visible"/> \n

// 자식 component의 model 옵션을 제거한다.`}}
          </code>
        </pre>
      </div>
      <div class="code">
        <h3>Vue3</h3>
        <pre>
          <code>
{{`// 부모 component
&lt;child-component v-model:visible="visible"/>`}}
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
  name: "ModelSync",
};
</script>

<style scoped></style>
