<template>
  <!-- kiri atas -->
  <q-page class="q-pa-md">
  <!-- tengah center -->
  <!-- <q-page class="flex flex-center"> -->
    
    <!-- lambang quasar yang ditengah -->
    <!-- <img alt="Quasar logo" src="~assets/quasar-logo-full.svg"> -->
    
    <!-- clear message tanpa method -->
    <!-- <button @click="message=''">Clear</button> -->
    <!-- clear message dengan method clearMessage -->
    <button @click="clearMessage">Clear</button>
    <!-- textbox -->
    <input v-model="message" @keyup="handleKeyUp"/>
    <H5>{{ message }}</H5>
  </q-page>
</template>

<script>
export default {
  data(){
    return{
      message:'Test Value'
    }
  },
  methods:{
    clearMessage(){
      this.message=''
    
    },
    handleKeyUp(e){
    if(e.keyCode==27){
      console.log(e)
      this.message='ESC'
      }
    }
  }
  
}
</script>
