 
      <template>
        <div>Файл App.Vue</div>
          <div class="app">
            <post-list/>
            <post-form/>


          </div>
 
      </template>

 

 <script>
import PostForm from "@/components/PostForm.vue";
import PostList from "@/components/PostList.vue";


export default{
components: {
  PostForm, PostList
},

  data(){
    return{
      // score:0,
      massive: [
        {number: 1, model: 'Samsung', price: 15000},
        {number: 2, model: 'Huawei', price: 17000},
        {number: 3, model: 'Realme', price: 13000},
      ],
      // Для отображения
      model: '',
      price: '',
      number: 4,
    }

  },
  methods: {
    addScore() {
      this.score+=1
    },
    inputModel(event) {
       this.model = event.target.value
      //  console.log(event.target.value.length);
    },
    inputPrice(event) {
       this.price = event.target.value
    },
    createPost(event) {
       event.preventDefault()
       const newPost = {
        id: Date.now(),
        model: this.model,
        price: this.price,
        number: this.number
      }
    this.massive.push(newPost),
    this.model = ''
    this.price = ''
    this.number += 1
    console.log(this.number)
    },
    clearPost (event) {
      this.model = ''
      this.price = ''
    }

  }
}

</script>






<style scoped>
 

</style>
 



