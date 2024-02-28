


<template>
    <div class="components">Файл PostCheck</div>
    <!--! обычный вариант -->
    <button @click="checkScore++">
        <slot>{{ checkScore }}</slot>
    </button>

    <!--! через функцию -->
    <button @click="checkButton">{{ checkScore2 }}</button>

    <!--! создание условия -->
    <div v-if="checkScore == 2">Сообщение:{{ info }}</div>

    <div v-if="checkScore >= 3 && checkScore <= 10">{{ info2 }}</div>
    
    <div style="margin-top: 25px;"> <span v-if="checkScore>=1">{{ info }}</span> Lorem ipsum dolor, sit amet consectetur adipisicing elit. Veritatis reiciendis facilis voluptas! Magni, at impedit.<br>
        <span style="color: red;" v-if="checkScore>=1">{{ info2 }}</span> In incidunt vero, veritatis quis distinctio sunt eveniet iure, asperiores blanditiis ea ducimus eaque et.</div>
</template>

<script>
export default {
    data() {
        return {
            info: 'Hello world',
            info2: 'Вы ушли слишком далеко',
            checkScore: 0,
            checkScore2: 0,
        }
        console.log(3);
    },
    methods: {
        checkButton() {
            this.checkScore2 += 1
        },
    },
}
</script>

<style scoped>
div {}
</style>