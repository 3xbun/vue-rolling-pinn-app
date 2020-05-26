<template>
  <div>
    <div id="btn">
      <button v-if="(title = 'add')">
        <i class="fas fa-plus"></i> New Sales
      </button>
    </div>
  </div>
</template>

<script>
export default {
  props: ["title"]
};
</script>

<style lang="scss" scoped>
#btn {
  width: 100%;
  margin: 3em auto;

  &:hover {
    cursor: pointer;
  }

  button {
    width: 100%;
    padding: 0.4em 1em;
    border-radius: 0.5em;
    border: none;
    background-color: #e7a6de;
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
    color: #fff;
    font-size: 2em;
  }
}
</style>
