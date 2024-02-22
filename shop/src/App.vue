 
      <template>

      <form>
        <h3>Новый пост</h3>
          <input 
          v-bind:value="model" 
          @input="inputTitle"
        
          class="element" 
          type="text" 
          placeholder="Название">

          <input 
          v-bind:value="price" 
          @input="inputPrice"
          class="element" 
          type="text" 
          placeholder="Описание">
          <!-- <input class="element" type="text" placeholder="Название">
          <input class="element" type="text" placeholder="Описание"> -->
        <button class="create" @click="createPost">Создать</button>
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
        {model: 'Sumsung', price: 15000},
        {model: 'Huawei', price: 17000},
        {model: 'Realme', price: 13000},
      ],
      model: '',
      price:''
    }
  },
  methods: {
    addScore() {
      this.score+=1
    },

    createPost() {
  
    },
    inputTitle(event) {
        this.model = event.target.value
    },
    inputPrice(event) {
        this.price = event.target.value
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
 .mass {
  border: 2px solid red;
  padding: 10px;
  margin-top: 15px;
}
.mass:hover {
  border: 2px solid orange;
  }
.element {
  width: 100%;
  padding: 10px;
  margin: 10px;
}

.create {
  margin-bottom: 55px;
  /* display: flex; */
  align-self: flex-end;
}
form {
  display: flex;
  flex-direction: column;
}

</style>
 



