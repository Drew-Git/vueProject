<template>
  <div class="menu">
    <a v-for="(item, i) in menu" :key="i"> {{item}} {{i}} </a>
  </div>

  <div>
    <img class="room-img" src="./assets/rooms/room0.jpg"/>
    <h4>{{products[0]}}</h4>
    <p>50만원</p>
    <button v-on:click="increase(0)"
            v-on:mouseover="reported[0]--">허위매물신고</button> <!-- v-on:click="" or @click="" -->
    <span> 신고수 : {{reported[0]}}</span>
  </div>

  <div>
    <img class="room-img" src="./assets/rooms/room1.jpg"/>
    <h4>{{products[1]}}</h4>
    <p>60만원</p>
    <button v-on:click="increase(1)"
            v-on:mouseover="reported[1]--">허위매물신고</button>
    <span> 신고수 : {{reported[1]}}</span>
  </div>

  <div>
    <img class="room-img" src="./assets/rooms/room2.jpg"/>
    <h4>{{products[2]}}</h4>
    <p>70만원</p>
    <button v-on:click="increase(2)"
            v-on:mouseover="reported[2]--">허위매물신고</button>
    <span> 신고수 : {{reported[2]}}</span>
  </div>

  <h3 class="pt30"> commented </h3>
  <!-- <div v-for="(item, i) in products" :key="i">
    <h4>{{item}}</h4>
    <p>{{productsPrice[i]}} 만원</p>
  </div>

  <h3 class="pt30"> tests </h3>
  <div v-for="(item, i) in products" :key="i">
    <h4>{{item}}</h4>
    <p>{{productsPrice[i]}} 만원</p>
  </div>

  <div class="pt30"></div>
  <div v-for="(items, i) in productsObj" :key="i">
    <div v-for="(item,j) in items" :key="j">
      <h4>{{j}}</h4>
      <p>{{item}} 만원</p>
    </div>
    <p>{{productsPrice[i]}} 만원</p> 
  </div> -->

  <a></a>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      reported : [0,0,0],
      price1 : 600,
      price2 : 700,
      logo : '원룸샵',
      products : ['역삼동원룸', '천호동원룸', '마포구원룸'],
      productsPrice : ['100', '200', '300'],
      productsObj : [{'역삼동원룸': '100'}, {'천호동원룸': '200'}, {'마포구원룸':'300'}],
      menu : ['HOME', 'SHOP', 'ABOUT']
    }
  },
  
  methods : {
    increase(i) {
      this.reported[i] += 1;
    }

  },

  components: {
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}

.menu a {
  color: white;
  padding : 10px;
}
.pt30 {
  padding-top: 30px;
}
.room-img {
  width:50%;
  margin-top :40px;
}
</style>












