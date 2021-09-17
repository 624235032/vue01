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
      <b>Id</b>: {{emp.id}},<br/>
      <b>Name</b>: {{emp.name}},<br/>
      <b>Salary</b>: {{emp.Salary}},<br/><br/><br/>
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
      employees:[{"id":1,"name":"John","Salary":30000},{"id":2,"name":"Trump","Salary":10000},{"id":3,"name":"Peter","Salary":99000}]


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
