 
      
      
      
      <template>
        
        
        <div class="app">
          <post-header/>  
          
          <!-- <post-entrance/> -->
          
          <post-advertisement/>
          
          <post-footer/>


 



            
            <!-- <post-form
            @create2="createPost"
            />  -->
            <!-- @create2 - передача данных из ребёнка к родителю -->

            <!-- <post-list 
               :massive="massive"
            /> -->
            <!-- или v-bind:massive="massive"  - отправка массива в postList-->
          </div>
      </template>



<script>   
import PostEntrance  from "@/components/PostEntrance.vue"
import PostHeader from "./components/PostHeader.vue";
import PostFooter from "./components/PostFooter.vue";
import PostAdvertisement from "./components/PostAdvertisement.vue";
// import PostForm from "./components/PostForm.vue";
// import PostList from "@/components/PostList.vue";





export default{
components: {
  PostHeader, PostEntrance, PostFooter, PostAdvertisement
  // PostForm, PostList, 
},

  data(){
    return{
      massive: [
        {number: 1, model: 'Samsung', price: 15000},
        {number: 2, model: 'Huawei', price: 17000},
        {number: 3, model: 'Realme', price: 13000},
      ],
    }
  },
  methods: {
    createPost(mass, second, third){
     this.massive.push(mass);
    },
  }
}

</script>





<style>

 button {
    color: aliceblue !important;
    padding: 5px;
    margin-top: 10px;
    background-color: crimson;
    width: 150px;
    height: 30px;
    cursor: pointer;
    border-radius: 5px;
  }
  .components {
    color: red;
    text-shadow: 2px 0px 8px white;
    font-size: 1.2em;
    margin-top: 25px;
}

</style>
 



