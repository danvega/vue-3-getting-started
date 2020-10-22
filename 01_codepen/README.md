# CodePen

If you're not familiar with CodePen it is this great online code editor that allows you to build, share and learn JavaScript, HTML and CSS. Did you know you can write Vue Single File Components (SFC) in CodePen? It isn't something that you can get to from the editor but if you go to a special URL you can open up a Vue editor and they have support for Vue 3.

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
