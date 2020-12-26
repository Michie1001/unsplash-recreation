<template>
  <div class="hello">
    <!-- <h1>{{ msg }}</h1> -->
    <header class="header">
      <input type="" name="" placeholder="Search for photo">
    </header>
    <div class="content">
      <div class="gridArea">
        <div class="photo">
          <!-- <img src=""> -->
          <div class="photo__Details">
            <p class="author">Jordan Okeke</p>
            <p class="location">Ogun, Nigeria</p>
          </div>
        </div>
        <div class="photo"></div>
        <div class="photo"></div>
        <div class="photo"></div>
      </div>
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
.content{
  padding: 0 20vw;
  margin-top: -5vh;
}
.gridArea{
  display: grid;
  justify-items: center;
  grid-template-columns: repeat(3, auto);
  grid-gap: 30px 60px;
}
.photo{
  background-color: blue;
  height: 250px;
  width: 100%;
  display: flex;
  align-items: flex-end;
  border-radius: 7px;
  box-shadow: inset 0px 0px 80px 0px rgba(0,0,0,0.8);
}
.photo__Details{
  color: #fff;
  padding: 7%;
}
p{
  margin: 10px 0 0;
}
.location{
  font-size: 11px;
}
</style>
