<template>
  <div>
    <WonderDetails :wonders="wonders"/>
  </div>
</template>

<script>

import WonderDetails from "@/components/WonderDetails";
export default {
  name: 'WondersList',
  components: {
    WonderDetails
  },
  props:{
    wonders: Array
  }
}
</script>

<style scoped>

</style>
