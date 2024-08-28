<script>
export default {
  name: 'KeyEvents',
  data() {
    return {
      fontSize: '16'
    }
  },
  methods: {
    incrementar() {
      this.fontSize++
    },
    disminuir() {
      this.fontSize--
    }
  }
}
</script>
<template>
  <input
    :style="{
      fontSize: `${fontSize}px`
    }"
    type="text"
    @keyup.ctrl.up="incrementar"
    @keyup.ctrl.down="disminuir"
  />
</template>
