<template>
  <div>
  <p> {{content}} </p>
  </div>
</template>

<script>
export default {
  name: 'FooterBar',
  props:{
    content: String
  }
}
</script>

<style scoped>
p{
  background: #0F2027;
  background: -webkit-linear-gradient(to right, #2C5364, #203A43, #0F2027);
  background: linear-gradient(to right, #2C5364, #203A43, #0F2027);
  color: #F2EFE7;
}

</style>