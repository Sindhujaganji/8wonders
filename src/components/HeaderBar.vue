<template>
  <h3> {{title}} </h3>
</template>

<script>


export default {
  name: 'HeaderBar',
  props: {
    title: String
  },
  components: {

  }
}
</script>

<style scoped>
h3{
  background: #0F2027;
  background: -webkit-linear-gradient(to right, #2C5364, #203A43, #0F2027);
  background: linear-gradient(to right, #2C5364, #203A43, #0F2027);
  color: #F2EFE7;;
}
</style>
