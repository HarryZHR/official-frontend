<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style lang="less">
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
  }
  body {
    padding: 0;
    margin: 0;
  }

  .border-blue {
    border: 1px solid #409EFF;
  }

  .width-1000 {
    width: 1000px;
    margin: 0 auto;
  }

  .float-left {
    float: left;
  }

  .float-right {
    float: right;
  }

  .clear {
    clear: both;
  }

  .tel {
    padding: 0 0 20px 60px;
    background: url("assets/images/tel.png") no-repeat;
    margin-top: 30px;
  }

  .block{
    display: block;
  }

  .color-blue {
    color: #409EFF;
  }

  .font-12 {
    font-size: 12px;
  }

  .font-14 {
    font-size: 14px;
  }

  .font-16 {
    font-size: 16px;
  }

  .font-20 {
    font-size: 20px;
  }

  .font-weight-bolder {
    font-weight: bolder;
  }

  .background-blue {
    background-color: #409EFF;
  }

  .background-black {
    background-color: #333;
  }

  .width-124 {
    width: 124px;
  }

  .width-350 {
    width: 350px;
  }

  .width-400 {
    width: 400px;
  }

  .background-grey {
    background-color: #D9D9D9;
  }

  .height-60 {
    height: 60px;
  }

  .height-40 {
    height: 40px;
  }

  .padding-top-20 {
    padding-top: 20px;
  }

  .padding-top-10 {
    padding-top: 10px;
  }

  .padding-10 {
    padding: 10px;
  }

  .padding-top-15 {
    padding-top: 15px;
  }

  ul {
    list-style: none;
  }
</style>
