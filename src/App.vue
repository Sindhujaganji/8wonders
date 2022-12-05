
<!--https://todolistjson.herokuapp.com/api-->
<template>
  <header>
    <HeaderBar title="The Great Wonders of the World "/>
  </header>
  <WondersList :wonders="wonders"/>
  <footer>
    <FooterBar content="&copy; Copyright 2022"/>
  </footer>
</template>

<script>

import HeaderBar from "@/components/HeaderBar";
import WondersList from "@/components/WondersList";
import FooterBar from "@/components/FooterBar";

export default {
  name: 'App',
  components: {
    FooterBar,
    HeaderBar,
    WondersList
  },
  data(){
    return{
      wonders: []
    };
  },
  async created(){
    this.wonders = await this.fetchData();
  },
  methods:{
    async fetchData(){
      const res = await fetch("https://todolistjson.herokuapp.com/api")
      const data = await res.json()
      console.log(data)
      return data.wonders
    }
  }
};
</script>

<style>
*{
  margin:0;
  padding:0;
  box-sizing: border-box;
  background-color: #F2EFE7;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

header{
  text-align: center;
  background: #0F2027;
  background: -webkit-linear-gradient(to right, #2C5364, #203A43, #0F2027);
  background: linear-gradient(to right, #2C5364, #203A43, #0F2027);
  color: #F2EFE7;
  padding: 30px;
}


footer{
  text-align: center;
  background: #0F2027;
  background: -webkit-linear-gradient(to right, #2C5364, #203A43, #0F2027);
  background: linear-gradient(to right, #2C5364, #203A43, #0F2027);
  color: #F2EFE7;
  padding: 20px;
  margin-top: 50px;
}


</style>
