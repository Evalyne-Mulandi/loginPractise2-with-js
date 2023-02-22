<template>
  <main class=" m-2">
    <div class=" flex justify-center items-center flex-col mx-auto">
        <h1>{{bookId}}</h1>
        <p>{{bookTitle}}</p>
        <h3>{{bookPages}}</h3>
    </div>

  </main>
</template>

<script>
export default {
props:[
'bookId',"bookTitle","bookPages" 
]
}
</script>

<style>

</style>