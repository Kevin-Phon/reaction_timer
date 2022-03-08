<template>
  <p>Score result is {{score}}</p>
  <div v-if="score<250">
      You are too fast. You must be cheat!👀😒
  </div>
  <div v-else-if="score>250 && score<500">
      Yes, that's normal.👍😘
  </div>
  <div v-else>
      Come on,Dude.Slow man,try again!😜😁
  </div>
</template>

<script>
export default {
    props:['score']
}
</script>

<style scoped>
    p{
        color: green;
    }
    div{
        color: aqua;
        font-size: 50px;
        font-style: italic;
        font-weight: bolder;
    }
</style>