# Vue3 + Vite + Vuetify Project

Hi everyone, welcome to the Vue demo project. The goal of this exercise is to generate a single page web app using Vue with Vuetify. In this project you'll be launching a local server, creating components, rendering those components, and edting a graph I created in advance. A lot of the boiler plate code has been created for you so that you can focus on learning Vue. Below are step-by-step instructions for you to follow. Additionally, if you run the command `git checkout solution` you'll see the final product and be able to compare your code as needed!

1. Fork Project ✅
2. Clone Project ✅
3. Install packages and run server ✅

# Understanding App.vue

Now that the project is setup, it's time to start using and working with Vue. As you can see we've currently got the default 'Welcome to the Vuetify 3 Beta' as our landing page. If you open the src folder inside of tutor-project you'll see App.vue, open it and look inside it. You will see two important pieces of code. The first is _template_:

```JavaScript
<template>
  <v-app>
    <v-main>
      <HelloWorld/>
    </v-main>
  </v-app>
</template>
```

Template is the HTML that we mount onto index.html in the tutor-project folder. If you look at index.html you will see `<div>#app</div>`. If you then go into the src folder and open main.js you will see the following: `createApp(App).use(vuetify).mount('#app')`. Here we are _mounting_ our Vue app onto index.html; mounting essentially means turning on Vue, just like flipping a light switch

You can think of the mounting process as a tree diagram that flows in this order: index.html > main.js > App.vue > ... all our components and views. index.html is our html bedrock and main.js is the connection between that raw html and Vue. index.html is our [DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction) whilst Vue is our [Virtual DOM](https://blog.logrocket.com/how-the-virtual-dom-works-in-vue-js/)... but we can ignore of all that for now!

Back on topic... specifically pay attention to `<HelloWorld />`, this is the component that is currently being rendered on your browser

**We have to place the component we want to render on the page inside of the template**

If you're wondering what v-app and v-main are, this is Vuetify wrapping our entire app. We can ignore this for now but we'll come back to this syntax later!

The next important code block is the _script_:

```JavaScript
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

The _script tag_ holds all of our JavaScript. In the first line we must import the component we want to use. As you can see we're importing the component by its name and navigating to the location where the file is stored. All of our components should be stored inside of src/components

Inside of export default we see that we have a method called components where we call the component once again. The import function above makes the component available to be used, but here is where we actually use it!

Without calling `<HelloWorld />` in the template, importing `HelloWorld` in the script AND calling the component inside of the component method, nothing would render! If you want to test it, comment out `<HelloWorld />` inside of the template and you'll see it disappear from the webpage! To comment something out, click on the line of code you want (or highlight it), then hit ctrl + / (cmd + / in MacOS)

You can comment out each HelloWorld piece of code, if any one of the three are missing nothing is rendered and errors are generated. You always want to follow the pattern of:

1. Place the `<Component />` inside of the template
2. Import the Component from the components folder
3. Call the Component inside of the components method

# Tasks

1. **Modify the Header component in src/components: change the title text and background color, then render it on App.vue (remember the three steps above!)**

I have set a default color on this header, but there are many ways to change it! For example the R2 blue color is `color="#0083cb"`, which is a Hex color code. You can use this [site](https://htmlcolorcodes.com/) to find a color you like! You can also use default colors such as 'black', 'blue', but a hex color reference is the best practice as you'd typically be given a Hex color from the lead designer

Depending on the color of your header, you might need to change the color of the title text using CSS to make it more readable! I have created an id for you: `#header-title` and referenced it in the `<style></style>` tag. You need to figure out how to change the font color using CSS (hint: use Google!)

Once you've done the above, congratulations! With a few lines of code you've created your first Navigation bar and [Single Page Web Application](https://developer.mozilla.org/en-US/docs/Glossary/SPA)

`v-app-bar` and `v-toolbar-title` are pre-made Vuetify components that we also made use of, you can read the documentation about them [here](https://vuetifyjs.com/en/components/app-bars/) and see what other parameters we can add. Additionally, using the documentation, the website can generate the code we need! Try changing the Elevation and color in the demo on the documentation page, are there any additional parameters you want to try on your Header component? Test them out!

2. **Create a Footer component in src/components: set it's color, and render it on App.vue**

Right click on the components folder, select new file, and name it Footer.vue

Now we need to add a Vuetify footer, you can find the documentation [here](https://vuetifyjs.com/en/components/footer/). Personally, I quite like Padless footer, so we can scroll to that section and click on the icon that looks like: <>, this will allow you to view the source code. Then we can just copy that entire code block and paste it in!

The next step is rendering the footer on the webpage, don't forget the three steps we outlined at the beginning!

You'll notice the code we copied calls a function to display the current year, with some text next to it that is 'strong' (bold). Feel free to change this text if you want to. Additionally, just as we set the color in the header we can do the same for the footer here! Note: in header we modified v-app-bar to set the color, in this instance we modify v-footer to change the color. We always target the Vuetify wrapper if we want to set a background color for something

Inside of the first footer tag, paste in this code: `absolute bottom padless width="100%"`, this will ensure that the footer remains at the bottom of the page and spreads across the entire page

Extra credit: Date() is an in-built function that is calling the method getFullYear(), this means that there are many other methods inside of Date() that we can use instead of getFullyear()! Research the JavaScript Date() method and experiment with the other methods

Extra extra credit: if i were to call Date().getDay(), what do you think I would get if I was calling the function on a Monday?

3. **Create an Title component in src/components: remove HelloWorld and add some text**

Create a new vue file as covered above and name it Title.vue, don't forget to add it to the template! Next we want to comment out the HelloWorld component on App.vue - but remember, there are 3 instances on App.vue where HelloWorld is mentioned: make sure you comment out all three!

Inside of the template we want to place a standard HTML title, but... we don't use the `<header></header>` or `<title></title>` tag. Instead we want to use a different tag, you can read about what you need to use and why [here](https://www.socialhive.com.au/blog/2021/june/h1-tags/#:~:text=HTML%20heading%20tags%20are%20used,language%20used%20to%20create%20websites.)

Then, create a `<div id='title'> </div>` and place the tag you created above between the > <

Once this is complete, render it on App.vue like the other components. Make sure it is below the Header component and above the footer component inside of the App.vue template. Feel free to experiment and place it above/below and see what happens!

You'll notice that the text is off to the left. Now create a `<style></style>` tag below the template. Inside here we refer to the div using the id we created like so:

```css
#title {
}
```

This allows us to specifically target and style just that div (divider). Work out how to align the text to the center!

4. **Create an About component in src/components: place it below the Title component**

Create a new component called About.vue, and create a template tag, followed by a`<script></script>` tag, and follow that with a style tag. Inside of the template create a html paragraph tag
