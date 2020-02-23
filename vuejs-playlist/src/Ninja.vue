<template>
  <div>
    <ul>
        <li v-for="ninja in Ninjas">
            {{ninja}}
        </li>
    </ul>
</div>
</template>

<script>
export default {
 data () {
    return {
      Ninjas: ['Lorenzo', 'Paolo', 'Marco']
    }
  }
}
</script>

<style>

</style>
