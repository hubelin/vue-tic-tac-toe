<template>
  <div>
    <button class="box" v-on:click="changeState">{{ boxText }}</button>
  </div>
</template>

<script>
export default {
  name: 'Box',
  props: ['boxText', 'idx'],
  methods: {
    changeState() {
      this.$emit('change', this.idx)
    }
  }
}
</script>

<style>
.box {
  height: 100px;
  width: 100px;
}
</style>
