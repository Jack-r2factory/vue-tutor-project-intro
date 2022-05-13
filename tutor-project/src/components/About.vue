<template>
  <div id="about-container">
    <p>
      {{ message }}
    </p>
  </div>
  <div id="img-container">
    <img
      src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/95/Vue.js_Logo_2.svg/1024px-Vue.js_Logo_2.svg.png?20170919082558"
    />
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: "Hello there!",
    };
  },
};
</script>

<style>
#about-container {
  text-align: center;
}

img {
  height: 200px;
  width: 200px;
}

#img-container {
  /* border: 2px solid red; */
  display: flex;
  justify-content: center;
  margin-top: 15px;
}
</style>
