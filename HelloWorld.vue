<template>
 <div id = "hello">
   <br />
   <h1>name : {{myName}}</h1>
   <h2>Tel : {{tel}}</h2>
   <h3>ID : {{ID}}</h3>

   <button>click me</button>
   <!-- <i class="fas fa-bahai"></i> -->
   <div class="btn-group" role="group" aria-label="Basic example">
  <button type="button" class="btn btn-secondary">Left</button>
  <button type="button" class="btn btn-secondary">Middle</button>
  <button type="button" class="btn btn-secondary">Right</button>
  </div>
  <!-- <i class="fas fa-bahai"></i>
  <b-card>hello</b-card> -->
  <br />
  <br />
 </div>
</template>

<script>
export default {
  name : "hello",
  data() {
    return {
      myName : "Piyakorn",
      tel: "0923476556",
      ID: "6130203381",
    };
  }
};
</script>

<style>
  #hello{
    background-color: rgb(195, 255, 126);
    color: rgb(70, 31, 8);
  }
</style>