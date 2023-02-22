<template>
   
<div> 
<Form/>
<Resources/>
<Button :message="message"/>
  <div class=" "  v-for="book in books" :key="book.id">
    <books :bookId="book.id" :bookTitle="book.title" :bookPages="book.pages"/>
  </div>
</div>
   
</template>

<script>
import Form from "./components/Form.vue";
import Resources from "./components/resources.vue";
import Button from "./components/button.vue";
 import books from "./components/books.vue";



export default {
  name: 'App',
  components: {
    Form,
    Resources,
    Button,
    books
},
data(){
  return{
  message:"Get started",
  books:[
{ id:1,title:"php",pages:"255",desc:"good programming language"},
{ id:2,title:"python",pages:"235",desc:"good programming language"},
{ id:3,title:"react",pages:"245",desc:"good programming language"},
{ id:4,title:"nuxt",pages:"225",desc:"good programming language"}

  ]
  }
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
  margin-top: 60px;
}
</style>
