<template>
  <div class="body">
    <h1>заголовок</h1>
    <p>Текса</p>
    <div class="step_list">
      <div class="item" v-for="item in items" :key="item">
        <p class="number p_black">{{ item.nubmer }}</p>
      </div>
    </div>
    <div class="but_row">
      <button class="but">Назад</button>
      <button class=" but">Далеее</button>
    </div>
  </div>
</template>

<script>

//import ItemModel from "./data/data_model"


export default {
  name: 'App',
  data() {
    return {
      title: "Название",
      index: 0,
      items: [
        {nubmer: 1, text: "q"},
        {nubmer: 2, text: "q"},
        {nubmer: 3, text: "q"},
        {nubmer: 4, text: "q"},
        {nubmer: 5, text: "q"},
      ],
    }
  }

}


</script>


<style>


.body {
  display: flex;
  flex-direction: column;
  justify-content: start;
  align-items: center;
  border-radius: 20px;
  margin: 0 auto;
  height: 300px;
  width: 1000px;
  background-color: white;
}

.step_list {
  width: inherit;
  display: flex;
  height: 50px;
  flex-direction: row;
  justify-content: start;

}


h1 {
  text-align: center;
}

.item {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  margin-left: 30px;
  background-color: lightgray;
  border-radius: 50%;
  height: 40px;
  width: 40px;
}

item_activ {
  color: greenyellow;
}

.number {
  margin: 0 auto;
  color: #42b983;
}

.p_black{
  color: black;
}

.p_white{
  color: white;
}

.but_row {
  width: 95%;
  display: flex;
  flex-direction: row;
  justify-content: start;
  align-items: center;
}

.but {
  padding: 5px 10px 5px 10px;
  margin-left: 10px;
  border-radius: 20px;
  border: 1.5px solid #42b983;
  color: #42b983;
  background-color: white;
}


</style>
