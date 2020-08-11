<template>
  <div class="vueMeteo card container">
      <h3> {{data.name}}</h3>
      <p> {{data.main.temp}} °</p>
      <img :src="data.iconPrefix + data.weather[0].icon + data.iconSuffix" alt="">
      <p>{{data.weather[0].description}}</p>

  </div>
</template>
<script>
    var prefix= "http://openweathermap.org/img/wn/";
    var suffix ="@2x.png";
export default {
    props: ['data'], // se mi arrivano da un altro componente NON sono DATA ma PROPS
    mounted() {
     // console.log(this.data);
    }

};

// var linkImg = "http://openweathermap.org/img/wn/" + data.weather[0].icon + "@2x.png";
// console.log(linkImg);
</script>

<style lang="scss">
  .vueMeteo {
    border-radius: 10px;
    background-image: url('https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fak0.picdn.net%2Fshutterstock%2Fvideos%2F1180270%2Fthumb%2F1.jpg&f=1&nofb=1');
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    border: 2px solid white;
    img {
      width: 150px;
      margin: 0 auto;
    }
    h3 {
      text-align: center;
    }
    p {
      text-align: center;
      text-transform: capitalize;
    }

  }
</style>
