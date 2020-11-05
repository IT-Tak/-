<template>
  <div>
    <p v-if="set" name='s'>123</p>
    <p v-else name='sd'>456</p>
  </div>
</template>

<script>
export default {
data(){
  return{
    set:true
  }
}
}
</script>

<style>

</style>