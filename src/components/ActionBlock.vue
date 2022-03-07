<template>
  <div class="block">
      Click here{{delay}}
  </div>
</template>

<script>
export default {
    props:['delay']
}
</script>

<style>
    .block{
        width: 300px;
        height: 200px;
        margin: 20px auto;
        background-color: aqua;
        padding: 20px;
        border-radius: 20px;
    }
</style>