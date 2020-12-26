<template>
  <div class="hello">
    <!-- <h1>{{ msg }}</h1> -->
    <header class="header">
      <input type="" name="" placeholder="Search for photo">
    </header>
    <div class="content">
      <div class="gridArea"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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

.header{
  background-color: #dce2e9;
  height: 30vh;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 0 10vw;
}
input{
  height: 40px;
  width: 100%;
  border: none;
  border-radius: 5px;
  text-indent: 10px;
  font-weight: bold;
}
</style>
