 
      <template>
        <div>Файл App.Vue</div>
          <div class="app">
            <post-form/>
            <post-list :massive="massive"/>
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
  // methods: {
  //   addScore() {
  //     this.score+=1
  //   },
  //   inputModel(event) {
  //      this.model = event.target.value
  //     //  console.log(event.target.value.length);
  //   },
  //   inputPrice(event) {
  //      this.price = event.target.value
  //   },
  //   createPost(event) {
  //      event.preventDefault()
  //      const newPost = {
  //       id: Date.now(),
  //       model: this.model,
  //       price: this.price,
  //       number: this.number
  //     }
  //   this.massive.push(newPost),
  //   this.model = ''
  //   this.price = ''
  //   this.number += 1
  //   console.log(this.number)
  //   },
  //   clearPost (event) {
  //     this.model = ''
  //     this.price = ''
    // }

  // }
}

</script>






<style scoped>
 

</style>
 



