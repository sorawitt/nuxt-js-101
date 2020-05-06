<template lang="html">
  <div>
    <p>Original message: "{{ message }}"</p>
    <p>Computed reversed message: "{{ reversedMessage }}"</p>
  </div></template
>

<script>
export default {
  data() {
    return {
      message: 'hello world'
    }
  },
  computed: {
    reversedMessage() {
      return this.message
        .split('')
        .reverse()
        .join('')
    }
  }
}
</script>

<style lang="css" scoped></style>
