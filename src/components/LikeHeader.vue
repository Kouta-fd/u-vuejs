<template>
  <slot name="title"></slot>
  <hr>
  <p>いいねの数</p>
  <slot name="number"></slot>
</template>

<script>
export default {
  props: ["headerText"]
};
</script>

<style >
h1 {
  color: red;
}
</style>
