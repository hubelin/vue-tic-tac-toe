<template>
  <div>
    <Box :boxText="boxState[0]" :idx="idx[0]" @change="updateState"></Box>
    <Box :boxText="boxState[1]" :idx="idx[1]" @change="updateState"></Box>
    <Box :boxText="boxState[2]" :idx="idx[2]" @change="updateState"></Box>
  </div>
</template>

<script>
import Box from './Box'
export default {
  props: ['boxState', 'idx'],
  components: {
    Box
  },
  methods: {
    updateState(boxIdx) {
      // console.log('in row', boxIdx)
      this.$emit('row', boxIdx)
    }
  }
}
</script>

<style></style>
