<template>
<div v-for="wonder in wonders" :key="wonder.id" class="details">
  <img :src= "wonder.image"  :alt="wonder.title">
  <div class="text">
  <h3> {{wonder.title}} </h3>
    <div class="para">
      <p> <span> Location: </span>  {{wonder.country}}</p>
      <p> <span> Bulit in: </span>  {{wonder.constructionDate}}</p>
      <p> <span> Built by: </span>  {{wonder.createdBy}}</p>
    </div>
    <p class="desc"> {{wonder.description}}</p>
  </div>
</div>
</template>

<script>

export default{
  name: 'WonderDetails',
  props:{
    wonders: Array
  },
}
</script>

<style scoped>
img{
  height: 210px;
  width: 250px;
}
.details{
  display: flex;
  background-color: #F2EFE7;
  padding: 20px 30px;
  box-shadow: 0px 0px 10px 5px  rgba(100,100,100,0.1);
  margin-top: 30px;
  margin-left: 20px;
  margin-right: 20px;
  border-right: 3px solid #0F2027;
  border-left: 3px solid #0F2027;
}
.text{
  margin-left: 40px;
  line-height: 1.5;
}
.para{
  margin-top: 10px;
}
.desc{
  margin-top: 10px;
  text-align: justify;
}
span{
  font-weight: bold;
}
</style>
