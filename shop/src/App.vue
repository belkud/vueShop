


<template>
   <div >{{ info }} {{ likes }}</div>
   <div >{{ someInfo }} {{ dislikes }}</div>
  <button type="button" @click="addLikes"> {{ likes }}</button>
  <button type="button" @mousemove="addDislikes"> {{ dislikes }}</button>

    <div class="post">
      <div>Название: Пост о телефонах</div>
      <div>Описание: Характеристики</div>
    </div>
    <div class="post">
      <div>Название: Пост о телефонах</div>
      <div>Описание: Характеристики</div>
    </div>
    <div class="post">
      <div>Название: Пост о телефонах</div>
      <div>Описание: Характеристики</div>
    </div>


</template>

  <script >
  // for (let posts of post) {

    
  // }
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
          addLikes() {
            this.likes +=1
            console.log(this.likes)
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
 .post {
  border: 2px solid red;
  padding: 10px;
  margin-top: 15px;
}
.post:hover {
  border: 2px solid orange;
  }
</style>
 