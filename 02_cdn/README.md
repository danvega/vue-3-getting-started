# Using a CDN

https://v3.vuejs.org/guide/introduction.html#declarative-rendering


Countdown Timer App

```html
    <div id="app">
      <h1>Hello, Vue 3!</h1>
      <p>{{ counter }}</p>
      <button @click="startCountdown">Start Countdown</button>
    </div>

    <script>
      const CountdownApp = {
        data() {
          return {
            counter: 10,
          };
        },
        methods: {
          startCountdown() {
            let timer = setInterval(() => {
              this.counter--;
              if (this.counter == 0) {
                clearInterval(timer);
              }
            }, 1000);
          },
        },
      };

      Vue.createApp(CountdownApp).mount("#app");
    </script>
```
