
<template>
  <div>Файл PostForm</div>
     <form>
        <h3>Создание списка</h3>

        
        <!-- v-bind - связывает данные -->
        <!-- @input - впечатывает (отслеживает) изменения -->
        <!-- -bind:value="mass.model"
        @input="mass.model=$event.target.value" -->

        <!--! v-model - тоже делает двустороннее связывание -->
        <input 
        v-model="mass.model"
        class="element" 
        type="text" 
        placeholder="Модель">
        
        <input 
        v-model="mass.price"
        class="element" 
        type="text" 
        placeholder="Стоимость">
          <div class="btn">
            <button @click="createPost">Создать</button>
            <button @click="" type="button">Очистить</button>
          </div>
        </form>
        

        <button type="button"  @click="addScore">Счёт{{ score }}</button>
        <button type="button2"  @click="addScore2">Счёт 2---{{ score2 }}</button>
</template>

<script >
export default {
  data(){
    return {
      score2: 0,
      mass: {
        model:'',
        price:'',
      }
    }
  },
  methods: {
    addScore2(event) {
      this.score2+=1
    },
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