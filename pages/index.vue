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
      message: 'hello world',
      firstName: 'Sorawit',
      lastName: 'Trutsat'
    }
  },
  computed: {
    fullName() {
      get() {
        return this.firstName + ' ' + this.lastName
      }

      set(val) {
        this.firstName = val.split(' ')[0]
        this.lastName = val.split(' ')[1]
      }
    }
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
