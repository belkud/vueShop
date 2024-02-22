 
 <template>

    <h3>Новый пост</h3>
    <input class="" type="text" placeholder="Название">
    <input class="" type="text" placeholder="Описание">
    <button>Создать</button>

    <button type="button" @click="addScore">{{ score }}</button>
    <div class="mass" v-for="mass in massive">Модель:{{ mass.model }}, Стоимость: {{ mass.price +score*100}}</div>
    <div @click="">fghfgh </div>
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
      ]
    }
  },
  methods: {
    addScore(e) {
      this.score+=1
    },
    check() {
      // this.x = (math.random())
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
}
.mass:hover {
  border: 2px solid orange;
  }


  
</style>
 



