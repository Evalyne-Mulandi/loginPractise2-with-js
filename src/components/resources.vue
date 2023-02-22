<template>
  
  <main>
    <div class="">dummy</div>
  </main>
</template>

<script>
export default {
    name: 'resources',
    data (){
      return{
           resources:[]  
        }
    },
    mounted(){
    this.fetchAllProducts()
    },
    methods:{
      async fetchAllProducts(){
        const res=await fetch("https://dummyjson.com/products")
        const json=await res.json()
        console.log(json);
        this.resources.push(json)
       l
      }
    }

}
</script>

<style>

</style>