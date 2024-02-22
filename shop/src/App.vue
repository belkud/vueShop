 
 <template>
    <button type="button" @click="addScore">{{ score }}</button>

      <div class="mass" v-for="mass in massive"  > Model: {{ mass.model }}, Device:{{ mass.cost }}рублей</div>
 

</template>



 <script>


export default{
  data(){
    return{
      score:0,
      massive:[
        {model:'sumsung', cost: 15000},
        {model:'huawei', cost: 18000},
        {model:'realme', cost: 17500},
      ],
    }
  },
  methods: {
    addScore() {
      this.score+=1
    },
  }
}
</script>











<style scoped>
  button {
    color: aliceblue !important;
    padding: 5px;
    margin-top: 10px;
    background-color: crimson;
    width: 150px;
    height: 30px;
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
 


<!-- <script setup="ts">
import App.vue from './App.vue'
<script> -->

<!-- <template>
  <button type="button" @click="addLikes"> {{ likes }}</button>
  <button type="button" @click="addDislikes"> {{ dislikes }}</button>

    <div class="post" v-for="post in posts">
      <div>Название:{{ post.title }}</div>
      <div>Описание: {{ post.body }}</div>
    </div>
  

</template>

  <script >

  export default {
      data() {
          return {
            likes: 0,
            dislikes: 0,
            posts:[
              {id:1, title:'JavaScript', body: 'Описание поста' },
              {id:2, title:'JavaScript 2', body: 'Описание поста 2' },
              {id:3, title:'JavaScript 3', body: 'Описание поста 3' },
            ]
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
  
  </script> -->
