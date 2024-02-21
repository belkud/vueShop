


<template>
   <div >{{ info }}</div>
   <div >{{ someInfo }}</div>
    <!-- <button type="button" @click="like">количество лайков: {{ like++ }}</button> -->
  <button type="button" @mousemove="this.info= 'что-то новенькое'"> Провести мышкой</button>
  <button type="button" @click="user()"> Нажать по клику</button>
  <button type="button" @click="user()"> Нажать по клику</button>
</template>

  <script>
  export default {
      data() {
          return {
            info:'Title' as any,
            someInfo:'Message',
            likes: 0
          }
      },
      methods: {
        user(chapter = 'bebebbebebebeb'){
          // this.info= 'что-то новенькое'
          this.info= chapter
        },
        likes() {
          this.likes +=1

        }
      }
  }

  </script>




<style scoped>
  button {
    color: aliceblue;
    padding: 5px;
    margin-top: 10px;
    background-color: crimson;
  }
 
  
</style>
 