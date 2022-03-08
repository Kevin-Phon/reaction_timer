<template>
  <div class="block" v-if="showBlock" @click="stopTimer()">
      Click here{{delay}}
  </div>
</template>

<script>
export default {
    props:['delay'],
    data(){
        return{
            showBlock : false,
            score : 0,
            timer : null
        }
    },
    mounted(){
        setTimeout(() => {
            this.showBlock = true
            this.startTimer()
        }, this.delay);
    },
    methods:{
        startTimer(){
            this.timer = setInterval(() => {
                this.score += 50
            }, 50);
        },
        stopTimer(){
            clearInterval(this.timer)
            this.$emit("endGame",this.score) 
        }
    }
}
</script>

<style scoped>
    .block{
        width: 300px;
        height: 200px;
        margin: 20px auto;
        background-color: aqua;
        padding: 20px;
        border-radius: 20px;
    }
</style>