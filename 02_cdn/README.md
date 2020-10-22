# Using a CDN

I want to talk about Vue being progressive here.

For prototyping or learning purposes, you can use the latest version with:

```
<script src="https://unpkg.com/vue@next"></script>
```

> Note: For production, we recommend linking to a specific version number and build to avoid unexpected breakage from newer versions.

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
