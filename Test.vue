<template>
  <div id="test" class="tmp2">
      <br />

<!-- input v-model -->
    <div class="input-group input-group-sm mb-3">
        <span class="input-group-text" id="inputGroup-sizing-sm">User</span>
        <input type="text" class="form-control" aria-label="Sizing example input" v-model="userName">
    </div>

    <div class="input-group mb-3">
        <span class="input-group-text" id="inputGroup-sizing-default">Password</span>
        <input type="text" class="form-control" aria-label="Sizing example input" v-model="userpass">
    </div>

    <div>
        shown<br>
        user: {{userName}} <br>
        password: {{userpass}} <br>
    </div>


<!-- ซ่อนชื่อ -->
    <div class="card">
        <div class="class-header primary">
            ชื่อ : {{myInfo.myName}}
            <button type="button" class="btn btn-secondary" v-on:click="myShowInfo">{{lableBotton}}</button>
        </div>

        <div class="class-body" :hidden="!hideShown">
            myNickname:{{myInfo.myNickname}},
            myStudentID: {{myInfo.myStudentID}},
        </div>
    </div>

    <b-button variant="dark" v-on:click="alertMsg('D', 'F', $event)">Click</b-button>
    <b-button variant="warning" v-on:dblclick='alertName'>Name</b-button>


<!-- รูป สุ่มหัวก้อย อุณหภูมิ -->
      <h1> HSW </h1>
      <img v-bind:src=url
      width="20%" height="20%"/>
      <img :src=url
      width="20%" height="20%"/>
      <br />
      <h2>fname : {{fname}}</h2>

    <br />
      <h2><span/> celsius :  {{celsius}}</h2>
      <h2><span/> fahrenheit : {{fahrenheit}}</h2>

      <h2> {{shown}} </h2>

  </div>
</template>

<script>
export default {
    name : "test",
    data(){
        return{
            fname: "FADE",
            imgName: "wooya",
            url: "https://pbs.twimg.com/media/E3axKtiVcAEAv2k.jpg",
            color: "tmp2",
            celsius: 30,
            dataPumu: ["หัว","ก้อย"],

            myInfo:{
                myName: "Piyakorn",
                myNickname:"bammm",
                myStudentID: "6130203381",
            },
            hideShown: true,

            userName : null,
            userpass: null,

            }
        },
        computed: {
            fahrenheit(){
                let result = (this.celsius*1.8) + 32;
                return result;
            },
            random() {
                return Math.random() > 0.5 ? 1 : 0;
            },
            shown() {
                return this.dataPumu[this.random];
            },
            lableBotton(){
                return this.hideShown ? "Hide" : "Shown";
            }
        },
        methods: {
            alertMsg(p1, p2, e){
                alert(`You ${e.type} the button at ${e.clientY}, ${e.clientY}`);
                alert(`parameter ${p1} , ${p2}`);
            },
            alertName(){
                console.log('bammm');
            },
            myShowInfo() {
                this.hideShown = !this.hideShown;
            }
        }
};
</script>

<style>
    .tmp{
        background-color: palevioletred;
        color: white;
    }
    .tmp2{
        background-color: skyblue;
        color: black;
    }
</style>