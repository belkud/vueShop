

<!-- 1. удалить файл base.css -->
<!-- 2. Возможно помочь со splice в PostEntrance  -->

<template>
    <div class=" flex pl-8 text-xl gap-16 mt-5 w-full">
        <div class=" cursor-pointer" @click="conFunc">Каталог &#128366;</div>
            <input placeholder="&#128269; Поиск по сайту" class=" border border-cyan-600 rounded-sm w-2/5 px-3 bg-gray-800"  >
                <div class=" cursor-pointer">Заказы 	&#128504;</div>
                <div class=" cursor-pointer">Избранное &#9829;</div>
            <div class=" cursor-pointer">Корзина &#128722</div>
        <div v-if="count%2==0" class=" cursor-pointer">Войти &#128274;</div>
        <div v-if="count%2!=0" class=" cursor-pointer">В айти &#128275;</div>
        <!-- text-3xl mt-3 p-5  text-3xl font-bold -->
    </div>

    
</template>

<script lang="ts">
export default {
    data(){
        return {
            count:0

        }
    }, methods: {
        conFunc(){
            this.count++
        }
    }
}
</script>

<style>
/* input {
    background-color: rgb(3, 35, 46); 
    color: aliceblue;
} */
</style>