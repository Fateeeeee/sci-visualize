<template>
  <div class="hello">
    <button id="b1">美丽科学</button>
    <button id="b2">视频中心</button>
    <button id="b3">全民制作平台</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
button{
  width:200px;
  height:90px;
  background-color: grey;
}
#b1{
  float: left;
  margin-left: 200px;
}
#b3{
  float: right;
  margin-right: 200px;
}
</style>
