<script setup>
import { ref } from 'vue';
import axios from "axios";
import ketboard from "../assets/鍵盤.png"
import mouse from "../assets/滑鼠.jpg"
import screen from "../assets/螢幕.jpg"
const test =()=>{
  axios
  .post("http://localhost:3001/create")
  .then((response)=>{
    console.log(response.data);
  })
}
const pay =()=>{
  
}
</script>

<template>
<div>
  <!-- header -->
  <div class="d-flex header justify-content-center align-items-center">
    <div class="HomeButton">Home</div>
    <div class="LoginButton">登入</div>
  </div>
  <!-- box -->
  <div class="box">
    <div class="d-flex fCardBox">
      <div class="fcard1" @click="pay">
        <div class="fcard1ImgBox">
          <img :src="ketboard" class="fcard1img">
          </div>
        <div class="fcard1text d-flex">
          <div class="col-4 TextSetIn a01"><b>New</b></div>
          <div class="col-8 d-flex flex-column">
            <div>這是一個鍵盤</div>
            <div class="PricceText">價錢999</div>
          </div>
        </div>
      </div>
      <div class="fcard1">
        <div class="fcard1ImgBox">
          <img :src="mouse" class="fcard1img">
          </div>
        <div class="fcard1text d-flex">
          <div class="col-4 TextSetIn a01"><b>New</b></div>
          <div class="col-8 d-flex flex-column">
            <div>這是一個滑鼠</div>
            <div class="PricceText">價錢99</div>
          </div>
        </div>
      </div>
      <div class="fcard1">
        <div class="fcard1ImgBox">
          <img :src="screen" class="fcard1img">
          </div>
        <div class="fcard1text d-flex">
          <div class="col-4 TextSetIn a01"><b>New</b></div>
          <div class="col-8 d-flex flex-column">
            <div>這是一個螢幕</div>
            <div class="PricceText">價錢9999</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
  
</template>

<style>
/* header */
.header{
  background-color: rgb(75, 75, 81);
  width: 100vw- 0.9rem;
  height: 10vh;
  max-height: 50px;
  min-height: 47px;
}
.HomeButton{
  border: 1px soild red;
  box-sizing: border-box;
  color: white;
  padding: 10px;
  height: 100%;
}
.HomeButton:hover{
  background-color: black;
  cursor: pointer;
}
.LoginButton{
  border: 1px soild aqua;
  box-sizing: border-box;
  color: white;
  padding: 10px;
  margin-left: auto;
  height: 100%;
}
.LoginButton:hover{
  background-color: black;
  cursor: pointer;
}
/* ================================================= */
/* box */
.box{
  background-color: antiquewhite;
  width: 100vw- 0.9rem;
  height: 100vh;
}
.fcard1{
  background-color: white;
  width: 200px;
  height: 200px;
  border: 2px solid black;
  box-sizing: border-box;
  margin: 10px;
}
.fcard2{
  background-color: blue;
  width: 200px;
  height: 200px;
}
.fcard3{
  background-color: purple;
  width: 200px;
  height: 200px;
}
.fcard1ImgBox{
  width: 100%;
  height: 75%;
}
.fcard1img{
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.fcard1text{
  height: 25%;
}
.a01{
  color: white;
  background-color: red;
}
.a02{

}
/* 文字置中====================================== */
.TextSetIn{
  display: flex;
  justify-content: center;
  align-items: center;
}
/* 文字置中====================================== */
/* 文字顏色大小================================== */
.PricceText{
  color: grey;
  font-size: 50%;
}
/* 文字顏色大小================================== */
</style>
