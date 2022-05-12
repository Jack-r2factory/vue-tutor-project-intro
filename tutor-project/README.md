# Vue3 + Vite + Vuetify Project

Hi everyone, welcome to the Vue demo project. The goal of this exercise is to generate a single page web app using Vue with Vuetify. In this project you'll be launching a local server, creating components, rendering those components, and edting a graph I created in advance. A lot of the boiler plate code has been created for you so that you can focus on learning Vue. Below are step-by-step instructions for you to follow. Additionally, if you run the command `git checkout solution` you'll see the final product and be able to compare your code as needed!

1. Fork Project ✅
2. Clone Project ✅
3. Install packages and run server ✅

## Understanding App.vue

Now that the project is setup, it's time to start using and working with Vue. As you can see we've currently got the default 'Welcome to the Vuetify 3 Beta' as our landing page. If you open the src folder inside of tutor-project you'll see App.vue, open it and look inside it. You will see two important pieces of code. The first is _template_:

```
<template>
  <v-app>
    <v-main>
      <HelloWorld/>
    </v-main>
  </v-app>
</template>
```

Template is the HTML that we mount onto index.html in the tutor-project folder, you can see this code inside main.js in the src folder: `createApp(App).use(vuetify).mount('#app')`. Specifically pay attention to `<HelloWorld />`, this is the component that is currently being rendered on your browser

**We have to place the component we want to render on the page inside of the template**

If you're wondering what v-app and v-main are, this is Vuetify wrapping our entire app. We can ignore this for now but we'll come back to this syntax later!

The next important code block is the _script_:

```
<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',

  components: {
    HelloWorld,
  },

  data: () => ({
    //
  }),
}
</script>
```

The _script tag_ holds all of our JavaScript. In the first line we must important the component we want to use. As you can see we're importing the component by its name and navigating to the location where the file is stored. All of our components should be stored inside of src/components

Inside of export default we see that we have a method called components where we call the component once again. The import function above makes the component available to be used, but here is where we actually use it!

Without calling `<HelloWorld />` in the template, importing `HelloWorld` in the script, and calling the component inside of the component method, nothing would render! If you want to test it, comment out `<HelloWorld />` inside of the template and you'll see it disappear from the webpage!
