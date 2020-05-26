<template>
  <div>
    <footer>{{ title }}</footer>
  </div>
</template>

<script>
export default {
  props: ["title"]
};
</script>

<style scoped>
footer {
  position: fixed;
  left: 0;
  bottom: 0;
  width: 100vw;
  background-color: #694b64;
  color: white;
  text-align: center;
  padding: 0.5em 1em;
  box-shadow: 0 -3px 6px rgba(0, 0, 0, 0.16), 0 3px 6px rgba(0, 0, 0, 0.23);
  font-size: 1.5em;
}
</style>
