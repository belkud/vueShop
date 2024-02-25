 
      <template>
        <div>Файл App.Vue</div>
          <div class="app">
            <post-list
               :massive="massive"
            />
            <post-form
               @create="createPost"
            /> 

            <!--или v-bind:massive="massive"  - отправка массива в postList-->

          </div>
 
      </template>

 

 <script>   
import PostForm from "@/components/PostForm.vue";
import PostList from "./components/PostList.vue";


export default{
components: {
  PostForm, PostList
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






<style scoped>
 

</style>
 



