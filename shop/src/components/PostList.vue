
<template>
  <div style="margin-top: 100px;">Файл PostList</div>
        <div class="mass" v-for="mass in massive">
          <div>Номер: {{ mass.number }}</div> 
          <div>Модель:{{ mass.model }}</div> 
          <div>Стоимость: {{ mass.price }}</div>
        </div>
</template>

<script>
  export default {
    props: {
      massive: {
        type: Array,
        required: true
      }
    }
  }

</script>



<style scoped>
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


</style>