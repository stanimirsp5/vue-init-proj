
<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
     <button v-on:click="addOne">Add 1</button>
     <!-- <button v-on:my-event="doSomething">Test event</button> -->
  <p>The button above has been clicked {{ counter }} times.</p>
  </div>
</template>
<script>
/* eslint-disable  */
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
    
  },
  data: function () {
    return {
      counter: 0
    }
  },
  methods:{
    addOne(){
      debugger
      this.counter++;
      this.$on('testevent', function (msg) {
          console.log(msg)
      })
    },
    doSomething(){
      console.log("in doSomething");

    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
