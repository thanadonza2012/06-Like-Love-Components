<template>
  <div>
    <p>ยอดคะแนนความชื่นชอบ {{ counter }} คะแนน.</p>
    <button @click="loveFunction()" class="btn btn-primary ml-2">🥰</button>
    <button @click="likeFunction()" class="btn btn-success ml-2">🙂</button>
    <button @click="samFunction()" class="btn btn-secondary ml-2">😐</button>
    <button @click="nolikeFunction()" class="btn btn-warning ml-2">🙁</button>
    <button @click="noloveFunction()" class="btn btn-danger ml-2">😡</button>
    <p v-bind:style="{fontSize: fsize - 'px'}"></p>
  </div>
</template>

<script>
export default {
  name: "CsBotton",
  data: function () {
    return {
      counter: 0,
      fsize: 60,
    };
  },
  props: {
    label: String,
  },
  methods: {
    loveFunction: function () {
      this.counter += 2;

    },
    likeFunction: function () {
      this.counter += 1;
    },
    samFunction: function () {
      this.counter += 0;

    },
    nolikeFunction: function () {
      this.counter -= 1;
 
    },
    noloveFunction: function () {
      this.counter -= 2;
 
    },
  },
};
</script>

<style>
</style>