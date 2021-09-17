<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <br/>
    <span>  {{message1}}  </span> <br/>
    <span v-text="message2" ></span>
    <hr/>
    <span>  {{counter}}  </span> <br/>
    <button v-on:click="counter=counter+1">+</button>
    <button v-on:click="minus">-</button>
    <hr/>
    <input v-bind:type="inputtype" />xxx<br/>
    <img v-bind:src="require(`@/assets/image/`+imagename)">
    
    <select v-model="messagename">
      <option value="StarWars.jpg">Image 1 </option>
      <option value="star.jpg">Image 2 </option>
      <option value="nb.png">Image 3 </option>
    </select>
    




    <input v-bind:type="inputtype" />

    <hr/>
    {{htmText}}<br/>
    <span v-html="htmlText"></span>
    


    <div v-bind:key="emp.id" v-for="emp in employees">
      <b>studentId</b>: {{emp.studentId}},<br/>
      <b>firstname</b>: {{emp.firstname}},<br/>
      <b>lastName</b>: {{emp.lastName}},<br/>
      <b>score</b>: {{emp.score}},<br/><br/><br/>
      </div>

    

    
    

  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    //HelloWorld
  },
  data(){
    return{
      message1: "Hello World!",
      message2: "Hello World Again!!",
      message3: "nattawut",
      inputtype: "text",
      imagename:"star.jpg",
      counter: 0,
      htmText: "student",
      isGreeting: true,
      employees:[{"studentId":624235032,"firstname":"nattawut","lastName":"bunwisoot","score":10},
                  {"studentId":624235000,"firstname":"kavid","lastName":"rober","score":7},
                  {"studentId":624235001,"firstname":"robert","lastName":"lewandowski","score":9},
                  {"studentId":624235002,"firstname":"lionel","lastName":"messi","score":10}]


    }
  },
  methods: {
    minus: function() {
      this.counter=this.counter-2
    }
  }

  


}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
