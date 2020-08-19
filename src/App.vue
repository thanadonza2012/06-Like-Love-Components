<template>
  <div id="app">
    <div class="row">
    <div class="col-4">
    <img alt="Vue logo" src="./assets/1.jpg" height="300px" width="300px">
     <CsBotton/>
    <img alt="Vue logo" src="./assets/2.jpg" height="300px" width="300px">
     <CsBotton/>
     </div>
     </div>
    <img alt="Vue logo" src="./assets/3.jpg" height="300px" width="300px">
     <CsBotton/>
    <img alt="Vue logo" src="./assets/4.jpg" height="300px" width="300px">
     <CsBotton/>
    <img alt="Vue logo" src="./assets/5.jpg" height="300px" width="300px">
     <CsBotton/>
    <img alt="Vue logo" src="./assets/6.jpg" height="300px" width="300px">
     <CsBotton/>
    <img alt="Vue logo" src="./assets/7.jpg" height="300px" width="300px">
     <CsBotton/>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <div class="row">
  
      
      <div class="col-6">
      </div>

      <div class="col-3"> <Counter lable="ok" @cc="sum"/> </div>
      <div class="col-3"> </div>
      <div class="col-3"> </div>

     <CsBotton/>
        
      

    </div>
    <div>
      ชื่อ-นามสกุล <input type="text" v-model="name"/>
      รหัส นศ. <input type="text " v-model="code">
      GPA <input type="number" v-model="gpa" step="0.01"/>
      <hr>
      แสดง ชื่อ + รหัส นศ. gpa 
    {{name}} {{code}} {{gpa}}
    </div>
    
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import CsBotton from './components/Csbotton'
export default {
  name: 'App',
  components: {
    HelloWorld,
    CsBotton,
  },
  data :function(){
    return{
    total:0,
    name:'',
    code:'',
    gpa:0.0,
    }
  },
  methods: {
    
    sum(counterValue) {
      this.total += counterValue
    },
  },
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