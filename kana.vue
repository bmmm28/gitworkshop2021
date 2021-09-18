<template>
  <div id="name" class="tmp">
      <br />
      <br />
      <h1>faculty : {{faculty}} </h1>
      <h2>program : {{program}}</h2>
      <br />
      <h2>{{pg01}}</h2>
      <h2>{{pg02}}</h2>
      <h2>{{pg03}}</h2>
      <h2>{{pg04}}</h2>
      <h2>{{pg05}}</h2>
      <h2>{{pg06}}</h2>
      <br />
      <br />

  </div>
</template>

<script>
export default {
    kana : "name",
    data() {
        return {
            faculty : "Science",
            program : "6 program",
            pg01 : "1.Information Technology",
            pg02 : "2.Computer Science",
            pg03 : "3.Department of Environmental Science",
            pg04 : "4.Chemistry",
            pg05 : "5.Applied Mathematics",
            pg06 : "6.Physics",
        };
    }
};
</script>

<style>
    #name{
        background-color: plum;
        color: rgb(70, 31, 8);
    }
</style>