


<template>
   <div >{{ info }}</div>
   <div >{{ someInfo }}</div>
    <!-- <button type="button" @click="like">количество лайков: {{ like++ }}</button> -->
  <button type="button" @mousemove="this.info= 'что-то новенькое'"> Провести мышкой</button>
  <button type="button" @click="this.info= 'что-то новенькое'"> Нажать по клику</button>
</template>

  <script  lang="ts">
  export default {
      data() {
          return {
            info:'Title' as any,
            someInfo:'Message'
          }
      },
      methods: {
        
      }
  }
  let like = 0
  </script>




<style scoped>
  button {
    color: aliceblue;
    padding: 5px;
    margin-top: 10px;
    background-color: crimson;
  }
 
  
</style>
 