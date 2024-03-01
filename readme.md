
<h3>Установка tailwind</h3>
```
https://tailwindcss.ru/docs/guides/vite/#vue
```



<h3>Работа с VUE</h3>

#### 1. Устанавливаем пакет
```
npm init vue@latest
 (npm init vite@latest <project-name> --template vue)???

``` 

#### 2. Выбираем VUE -> TypeScript 
#### Пишем cd (название проекта) , npm install , npm run dev


#### 3. Основные способы установки VUE (подробная инструкция)
```
https://v3.ru.vuejs.org/ru/guide/installation.html#%D0%B8%D1%81%D1%82%D0%BE%D1%80%D0%B8%D1%8F-%D0%B8%D0%B7%D0%BC%D0%B5%D0%BD%D0%B5%D0%BD%D0%B8%D0%B8
```
P.S. Если выскакивают ошибки при установке модулей
```
https://www.youtube.com/watch?v=vObwhyh5h5I&t=93s
```

---
---

<!-- #### P.S. Серверная часть находится в директории  -->
<!-- #### Клиентская часть находится в директории  -->
#### P.S. cd.. (название папки) - добавляет данную папку в директорию; cd - убирает последнюю папку в директории

или:

#### P.P.S. Для принудительного изменения директории: 
#### 1. 'ctrl' + '<' 
#### 2. в появившейся строке пишем 

```
Terminal.integrated.cwd
```

#### 3. пишем свою директорию 

<!--!!!!!!!!!! C:\GitHub_folders\nodeServer-9>  -->
---
---


 <h3>Работа с призмой </h3>
 
[![](https://s18955.pcdn.co/wp-content/uploads/2018/02/github.png)](https://github.com/user/repository/subscription)

#### 1. Инициализация призмы 
```
npm i
``` 

#### 2. Генерирует клиента Prisma на основе схемы 
```
npx prisma generate
```
 

#### 3. Синхронизирует состояние схемы Prisma с БД #### 
```
npx prisma db push
``` 
 

#### 4. Просмотр и управление данными через браузер
```
npx prisma studio
```
 

#### P.S. если нету файла .env, то обязательно его создать
```
DATABASE_URL="postgresql://postgres:(Пароль)@localhost:5432/(название таблицы)?schema=public"
```
 
#### P.P.S. чтобы не было ошибок в любом случае открываем pgAdmin и в нём если нету создаём одноимённую таблицу такую же как и в DATABASE_URL 
---
---
  

Котэ =^-^= (https://img.razrisyika.ru/kart/24/1200/94318-kot-saymon-4.jpg)
