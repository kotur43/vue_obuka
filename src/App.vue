<template>
  <div id="main">
    <img alt="Vue logo" src="./assets/logo.png">
    <h1>{{title}}</h1>
    <button @click="changeNumber('plus')">+</button>
    <h3>{{number}}</h3>
    <button @click="changeNumber('minus')">-</button>
  </div>
</template>

<script>

export default {
  data() {
    return {
      title: 'VUE OBUKA',
      number: 0

    }
  },
  methods: {
    addNumber(){
      this.number1 = this.number1 + 1
    },
    removeNumber(){
      this.number1 = this.number1 - 1
    },
    changeNumber(operation){
      if (operation == 'plus') {
        this.number++;
      } else if(operation == 'minus') {
        this.number--;
      }
      console.log(this.number)

      this.title = this.title + ' ' + this.number

    }
  },
}
</script>

<style>
#main {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
