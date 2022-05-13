<template>
  <div id="about-container">
    <p>
      {{ message }}
    </p>
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
</style>
