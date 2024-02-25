
<template>
  <div>Файл PostForm</div>
     <form>
        <h3>Создание списка</h3>

        
        <!-- v-bind - связывает данные -->
        <!-- @input - впечатывает (отслеживает) изменения -->
        
        <!-- ! v-bind="model.value" -->
        <input 
        @input="inputModel"
        v-bind:value="model"
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
            <button @click="" type="button">Очистить</button>
          </div>
        </form>
        

        <button type="button"  @click="addScore">{{ score }}</button>
</template>

<script >
import Drawer from '@/App.vue'
import { ref } from 'vue'



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