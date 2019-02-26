<template>
  <div id="app" class="container">
    <Row
      @row="updateBoxState"
      :boxState="[boxState[1], boxState[2], boxState[3]]"
      :idx="[1, 2, 3]"
    ></Row>
    <Row
      @row="updateBoxState"
      :boxState="[boxState[4], boxState[5], boxState[6]]"
      :idx="[4, 5, 6]"
    ></Row>
    <Row
      @row="updateBoxState"
      :boxState="[boxState[7], boxState[8], boxState[9]]"
      :idx="[7, 8, 9]"
    ></Row>
  </div>
</template>

<script>
import Row from './components/Row'
export default {
  data() {
    return {
      boxState: {
        1: 'X',
        2: 'X',
        3: 'X',
        4: 'X',
        5: 'X',
        6: 'X',
        7: 'X',
        8: 'X',
        9: 'X'
      }
    }
  },
  components: {
    Row
  },
  methods: {
    updateBoxState(idx) {
      console.log(this.boxState[idx])
      if (this.boxState[idx] === 'X') {
        this.boxState[idx] = 'O'
      } else {
        this.boxState[idx] = 'X'
      }
    }
  }
}
</script>

<style>
.container {
  display: grid;
  grid-template-columns: 100px 100px 100px;
}
</style>
