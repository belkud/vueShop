 
      <template>

      <form>
        <h3>Создание списка</h3>

        
        <input 
        v-bind="model.value"
        @input="inputModel"
        class="element" 
        type="text" 
        placeholder="Модель">
        
        <input 
        v-bind="price.value"
        @input="inputPrice"
        class="element" 
        type="text" 
        placeholder="Стоимость">
          <div class="btn">
            <button @click="createPost">Создать</button>
            <button @click="clearPost" type="button">Очистить</button>
          </div>
        </form>
        
        <div class="mass" v-for="mass in massive">
          <div>Модель:{{ mass.model }}</div> 
          <div>Стоимость: {{ mass.price }}</div>
        </div>
        <button type="button"  @click="addScore">{{ score }}</button>
      </template>



 <script>

export default{
  data(){
    return{
      score:0,
      massive: [
        {model: 'Samsung', price: 15000},
        {model: 'Huawei', price: 17000},
        {model: 'Realme', price: 13000},
      ],
      model: '',
      price: '',
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
        id: Date.now(),
        model: this.model,
        price:this.price
      }
    this.massive.push(newPost),
    this.model = ''
      this.price = ''



      console.log(Date.now());
    },
    clearPost (event) {
      this.model = ''
      this.price = ''
    }
    
  }
}

</script>




      <!-- <template>

      <form>
        <h3>Создание списка</h3>

        
        <input 
        v-bind:value="model" 
        @input="inputTitle"
        class="element" 
        type="text" 
        placeholder="Модель">
        
        <input 
        v-bind:value="price" 
        @input="inputPrice"
        class="element" 
        type="text" 
        placeholder="Стоимость">
          <div class="btn">
            <button @click="createPost">Создать</button>
            <button @click="clearPost" type="button">Очистить</button>
          </div>
        </form>
        
        <div class="mass" v-for="mass in massive">
          <div>Модель:{{ mass.model }}</div> 
          <div>Стоимость: {{ mass.price }}</div>
        </div>
        <button type="button"  @click="addScore">{{ score }}</button>
      </template>



 <script>

export default{
  data(){
    return{
      score:0,
      massive: [
        {model: 'Samsung', price: 15000},
        {model: 'Huawei', price: 17000},
        {model: 'Realme', price: 13000},
      ],
      model:'',
      price:''
    }

  },
  methods: {
    addScore() {
      this.score+=1
    },
    inputTitle(event) {
      this.model = event.target.value
    },
    inputPrice(event) {
      this.price = event.target.value
    },
    createPost(event) {
      event.preventDefault()
      const newPost = {
        id: Date.now(),
        id: Date.now(),
        model: this.model,
        price: this.price,

      }
      this.massive.push(newPost)
      this.model = ''
      this.price = ''
    },
    clearPost(event) {
      this.model = ''
      this.price = ''
    },
  }
}

</script> -->











<style scoped>
  button {
    color: aliceblue !important;
    padding: 5px;
    margin-top: 10px;
    background-color: crimson;
    width: 150px;
    height: 30px;
  }
 .mass {
  border: 2px solid red;
  padding: 10px;
  margin-top: 15px;
  /* position: absolute; */
  /* width: 100%; */
}
.mass:hover {
  border: 2px solid orange;
  transition: .3s;

  }
.element {
  width: 100%;
  padding: 10px;
  margin: 10px;
}

.btn {
  margin-bottom: 55px;
  align-self: flex-end;
}
.btn>button{
  margin: 10px;
}

form {
  display: flex;
  flex-direction: column;
}

</style>
 



