<template>
  <div>
    {{ message }}

    <button @click="reverseMessage"></button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: 'Hello Vue!'
    }
  },
  methods: {
    reverseMessage() {
      return (this.message = this.message
        .split('')
        .reverse()
        .join(''))
    }
  }
}
</script>

<style></style>
