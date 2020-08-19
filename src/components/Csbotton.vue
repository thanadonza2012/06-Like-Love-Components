<template>
 <div>
  <button @click="counter += 1">Add 1</button>
  
    <p>The button above has been clicked {{ counter }} times.</p>
    <p v-bind:style="{fontSize: fsize + 'px'}">Hello</p>
    <button @click="upFunction()" class ="btn btn-info"> 👍 </button>
    <button @click="downFunction()" class ="btn btn-info"> <i class="fa fa-angry"></i> </button>
       <p v-bind:style="{fontSize: fsize - 'px'}"></p>
        </div> 
 
</template>

<script>
export default {
    name: 'CsBotton',
    data: function() {
  return{
    counter: 0,
    fsize:60,
    }
  },
  props:{
    label:String,
    
  },
  methods : {
  upFunction: function(){
    this.counter += 1
    this.fsize += 10
  this.$emit('cc',this.fsize)

    console.log(this.fsize);
    console.log(this.counter);
  },
    downFunction: function(){
    this.counter -= 1
    this.fsize -= 10

    console.log(this.fsize);
    console.log(this.counter);
    },
  },
}
</script>

<style>

</style>