<template>
  <div :style="styleObject" class="test">
    <h1>Why is styleObject [object Object] on initial load during dev?</h1>
    <h4>although width and height are present?</h4>
    <h6>But `color: green` is applied immediately?</h6>
    <pre>width: {{ width }}</pre>
    <pre>height: {{ height }}</pre>
    <pre>{{ styleObject }}</pre>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',

  data () {
    return {
      width: 800,
      height: 600,
    }
  },

  computed: {
    styleObject () {
      return {
        color: 'green',
        aspectRatio: this.width / this.height,
      }
    },
  },
}
</script>

<style>
.test {
  width: 100%;
  background: lightcoral;

  padding: 20px;
}
</style>
