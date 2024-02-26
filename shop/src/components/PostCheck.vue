<template>
    <div class="components">Файл PostCheck</div>
    <button @click="checkButton"> {{ checkScore }}</button>
</template>

<script>
export default {
    data(){
        return {
            checkScore: 0
        }
    },
    methods: {
        checkButton(){
            this.checkScore+=1
        },
    },
}
</script>

<style scoped>

div {
}
</style>