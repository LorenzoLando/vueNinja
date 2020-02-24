<template>
  <div>
    <app-header></app-header>
    <app-ninja></app-ninja>
    <app-footer></app-footer>
  </div>
</template>

<script>
//1-importing the component
//2-registering locally the component
import Header from './components/Header.vue' //1
import Footer from './components/Footer.vue' //1
import Ninja from './components/Ninjas.vue' //1
export default {
  components: {
    'app-header': Header, //2
    'app-footer': Footer,
    'app-ninja': Ninja
  },
 data () {
    return {
      
    }
  }
}
</script>

<style>

</style>
