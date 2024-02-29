

<template>
<div class="menu">
    <h3>Вход на сайт</h3>
    <div>
        
    </div>
    <input type="text" v-model="name" placeholder="Имя">
    <input type="text" v-model="surname" placeholder="Фамилия">
    <input type="text" v-model="mail" placeholder="Почта">
    
    <div class="error">{{ this.error }}</div>
    <button @click="sendInfo"> Отправить</button>
    <div>{{ users }}</div>
    <!-- <div>вывод ошибки</div> -->
    <!-- (в конце разные цвета border) -->
</div>
</template>


<script>

    export default {
        data(){
            return{
                name:'',
                surname:'',
                mail:'',
                users:[],
                error:'',
            }
        }, methods:{
            sendInfo(){
                if (this.name=='') {
                    this.error = '(Введите имя)'
                  return 
                } else if(this.surname=='') {
    this.error= 'Введите фамилию'
    return
} else if (this.mail=='') {
    this.error = 'Введите почту'
    return
}


                this.users.push({
                    name: this.name,
                    surname: this.surname,
                    mail: this.mail,
                    users:[]
                })
                console.log(this.users)
            }
        }
    }

</script>









<style>
.menu{
    display: flex;
    flex-direction: column;
    gap: 20px;
}
.menu>input{
    padding: 10px;
    border-radius: 5px;
    /* width: 50%; */
    margin: 0 auto;
}
.error {
    padding: 0px;
    margin: 0 auto;
}
</style>























<!-- <template>
    <div style="color: greenyellow;" class="components">PostCheck</div>
    <div>Вычисление: <span v-if="score>=1">{{ info }}</span></div>
    <button type="button" @click="addScore()">{{ score }}</button>
    <div v-if="score<=10"> скрыть элемент после 10</div>
    <div v-if="score>=3">первый абзац</div>
    <div v-if="score>=6">второй абзац</div>

    <input type="text" placeholder="name" v-model="name">
    <input style="margin-left:10px ;" type="text" placeholder="email" v-model="mail">
    <div class="flex">
        <button @click="sendInfo()"> Отправить</button>
        
        <p>массив: {{ users }} <br></p>
        <p >ошибка: {{ error }} <br></p>
        
        <div>имя: {{ name }}</div>
        <div>почта: {{ mail }}</div>
    </div>

</template>

<script>

export default {
    data() {
        return {
            users: [],
            score: 0,
            info: 'первый',
            name:'',
            mail: '',
            error:'',
        }
    },
    methods: {
        addScore() {
            this.score++
            this.info = 'hello'
        },
        sendInfo(){
            if (this.name=='') {
                this.error='Введите имя'
                return
            } else if (this.mail=='') {
                this.error='Введите почту'
                return
            } else {
                this.error = ''
                
            }

            this.users.push({
                name: this.name,
                mail: this.mail,
            })
            console.log(this.name);
        }
    }
}

</script>

<style scoped>
.flex {
    margin-top: 10px;
}


</style>

 -->



















<!--!!!!!!!!!!!!!!!!!! ОТСЮДА НЕ УДАЛЯТЬ! -->

<!-- <template> -->
    <!-- <div class="components">Файл PostCheck</div> -->
    <!--! обычный вариант -->
    <!-- <button @click="checkScore++"> -->
        <!-- <slot>{{ checkScore }}</slot> -->
    <!-- </button> -->

    <!--! через функцию -->
    <!-- <button @click="checkButton">{{ checkScore2 }}</button> -->

    <!--! создание условия -->
    <!-- <div v-if="checkScore == 2">Сообщение:{{ info }}</div> -->

    <!-- <div v-if="checkScore >= 3 && checkScore <= 10">{{ info2 }}</div> -->
    
    <!-- <div style="margin-top: 25px;"> <span v-if="checkScore>=1">{{ info }}</span> Lorem ipsum dolor, sit amet consectetur adipisicing elit. Veritatis reiciendis facilis voluptas! Magni, at impedit.<br> -->
        <!-- <span style="color: red;" v-if="checkScore>=1">{{ info2 }}</span> In incidunt vero, veritatis quis distinctio sunt eveniet iure, asperiores blanditiis ea ducimus eaque et.</div> -->
<!-- </template> -->

<!-- <script>
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
</script> -->




<!-- <style scoped>
.changeColor {
    color: red;
}
</style> -->