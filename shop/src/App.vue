


<template>
   <div >{{ info }}</div>
   <div >{{ someInfo }}</div>
    <!-- <button type="button" @click="like">количество лайков: {{ like++ }}</button> -->
  <button type="button" @mousemove="this.info= 'что-то новенькое'"> Провести мышкой</button>
  <button type="button" v-on:click="addLikes"> {{ likes }}</button>
  <button type="button" v-on:click="addDislikes"> {{ dislikes }}</button>
</template>

  <script >
  export default {
      data() {
          return {
            info:'Title' ,
            someInfo:'Message',
            likes: 0,
            dislikes: 0,
          }
      },
      methods: {
        user(chapter = 'bebebbebebebeb'){
          // this.info= 'что-то новенькое'
          this.info= chapter
        },
        addLikes() {
          this.likes +=1
        },
        addDislikes () {
          this.dislikes -=1
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
    width: 150px;
  }
 
  
</style>
 