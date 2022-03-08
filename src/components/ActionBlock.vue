<template>
  <div class="block" v-if="showBlock">
      Click here{{delay}}
  </div>
</template>

<script>
export default {
    props:['delay'],
    data(){
        return{
            showBlock : false
        }
    },
    mounted(){
        setTimeout(() => {
            this.showBlock = true //data is update now so updated() work
        }, this.delay);
    },
    // updated(){
    //     console.log("data updated")
    // }
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