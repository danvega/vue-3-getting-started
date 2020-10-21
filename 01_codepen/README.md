# CodePen

Did you know you can write Single File Components in CodePen?

https://codepen.io/pen/editor/vue

> Note: Make sure to switch to Vue 3

```js
<template>
  <h1>Hello, Vue 3!</h1>
  <p>{{ now }}</p>
</template>

<script>
export default {
  data() {
    return {
      now: new Date().toString()
    };
  },
  methods: {
    updateDateTime() {
      this.now = new Date().toString()
    }
  },
  mounted() {
    setInterval(() => {
      this.updateDateTime();
    }, 1000);
  }
};
</script>

<style>
body {
  min-height: 100vh;
  background-color: #41b883;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  color: white;
}
h1 {
  text-transform: uppercase;
}
</style>

```
