<template>
  <div class="hello">
    <!-- <h1>{{ msg }}</h1> -->
    <header class="header">
      <input type="" name="" placeholder="Search for photo" id="search" v-on:keyup.enter="searchPhotos()">
      <button v-on:click="searchPhotos()">></button>
    </header>
    <div class="content">
      <div class="gridArea" id="results">
        <img :src="photos">
        <!-- <div class="photo">
          <div class="photo__Details">
            <p class="author">Jordan Okeke</p>
            <p class="location">Ogun, Nigeria</p>
          </div>
        </div> -->
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Landing',
  props: {
    msg: String,
  },
  data: function() {
    return {
      photos: ''
    };
  },
  methods: {
    searchPhotos(){
      let clientId = '5EdbUqaT9TTDMeUhgBNI6wCCESMDlVmKbs8banRc8jg';
      let query = document.getElementById("search").value;
      let url = `https://api.unsplash.com/photos/?client_id=${clientId}&query=${query}`;

      fetch(url)
      .then(function (data){
        return data.json();
      })
      .then(function(data){
        console.log(data);

        data.forEach(photo => {
          let result = `
            ${photo.urls.regular}
            ${photo.height}
            ${photo.user.name}
            ${photo.user.location}
          `;
          console.log(result);
          // this.photos = result;
        });
      })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
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
  .gridArea{
    display: grid;
    justify-items: center;
    grid-template-columns: repeat(3, auto);
    grid-template-rows: minmax(150px, auto);
    grid-gap: 30px 60px;
  }
}
.photo{
  background-color: blue;
  height: 250px;
  width: 100%;
  display: flex;
  align-items: flex-end;
  border-radius: 7px;
  box-shadow: inset 0px 0px 80px 0px rgba(0,0,0,0.8);
  
  .photo__Details{
    color: #fff;
    padding: 7%;
    
    .location{
      font-size: 11px;
    }
  }
}
p{
  margin: 10px 0 0;
}
</style>
