 
      <template>

      <form>
        <h3>Создание списка</h3>

        
        <!-- v-bind - связывает данные  (с vue.devTools появляется в input-е) -->
        <!-- @input - печатает (отслеживает) изменения -->
        
        <!--! v-bind="model.value" -->
        <input 
        v-bind:value="model"
        @input="inputModel"
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
          <div>Номер: {{ mass.number }}</div> 
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
       console.log(event.target.value.length);
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
 



