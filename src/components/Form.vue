<template>
  <div class=""> 
    <form
    @submit.prevent="handleSubmit"
    
    class=" flex justify-center items-center flex-col mx-auto max-w-lg gap-y-2 bg-slate-300 border-cyan-50 border rounded-md">
          <img src="" alt="" class=" flex justify-center items-center mx-auto p-1 rounded-full bg-white">
           
        <div class="flex justify-center items-center   flex-col ">
            <label  class=" text-black font-mono">F.Name</label>
        <input type="text" class="px-6 py-2 rounded-lg p-2 text-black m-1 "
         placeholder="Enter your first name" v-model="fname">
        </div>

        <div class="flex justify-center items-center   flex-col ">
            <label  class=" text-black font-mono">S.Name</label> 
        <input type="text" class="px-6 py-2 rounded-lg p-2 text-black m-1 "
         placeholder="Enter your Second name" v-model="sname">
        </div>

        <div class="flex justify-center items-center    flex-col ">
            <label  class=" text-black font-mono">PhoneNo</label>
         
        <input type="text" class="px-6 py-2 rounded-lg p-2 text-black m-1 "
         placeholder="Enter your phone number" v-model="phoneNo">
        </div>
        <div class="flex justify-center items-center    flex-col ">
            <label  class=" text-black font-mono">Email</label>
         
        <input type="Email" class="px-6 py-2 rounded-lg p-2 text-black m-1 "
         placeholder="Enter your email"  v-model=" email" required>
        </div>
        <input type="submit" class="px-6 py-2 rounded-lg p-2 text-white m-1  bg-black" 
        value="Submit">
    </form>
    <div 
    v-show="data"
    class="flex flex-col justify-center items-center mx-auto p-2 max-w-lg  bg-orange-500 text-black rounded-md  border-emerald-50 border">
        <h4 class=" font-extrabold">Output Data</h4>
        <fieldset class="flex justify-center items-center  flex-col ">
           
              <h5>{{fname}}</h5>
              <h5>{{sname}}</h5>
              <h5>{{phoneNo}}</h5>
              <h5>{{email}}</h5>
         
    
        </fieldset>
    </div>
  </div>
</template>

<script>
export default {
name:"FormVue",
data() { 
    return{ 
        fname:" ",
        sname:"",
        phoneNo:"",
        email:"",
        data: false
    }

},methods:{
    handleSubmit(){
        this.data=true

    }
 }

}
</script>

<style>

</style>