<template>
  <div id="ninjas">
    <!-- 1 on click change value of the show property -->
    <!-- 2 the element is rener just if v-for retunr true -->
      <ul>
          <li v-for="ninja in ninjas" v-on:click="ninja.show = !ninja.show"> <!-- 1 -->
              <h2>{{ninja.name}}</h2>
              <h3 v-if="ninja.show">{{ninja.speciality}}</h3> <!-- 2 -->
          </li>
      </ul>
  </div>
</template>

<script>
export default {
 data () {
    return {
      ninjas: [
          {name:'Lorenzo', speciality: 'Strategy', show: false},
          {name:'Puffo1', speciality: 'Mangiare', show: false},
          {name:'Puffo2', speciality: 'Bere', show: false},
          {name:'Puffo3', speciality: 'Dormire', show: false},
          {name:'Puffo4', speciality: 'Sognare', show: false},
          {name:'Puffo5', speciality: 'Fregare', show: false}
      ]
    }
  },
  methods: {
     showSpecility: function(){
         return this.ninjas.show = true
     } 
  }
}
</script>

<style scoped>
#ninjas{
    width: 100%;
    max-width: 1200px;
    margin: 40px auto;
    padding: 0 20px;
    box-sizing: border-box;
}
ul{
    display: flex;
    flex-wrap: wrap;
    list-style-type: none;
    padding: 0;
}
li{
    flex-grow: 1;
    flex-basis: 300px;
    text-align: center;
    padding: 30px;
    border: 1px solid #222;
    margin: 10px;
}
</style>
