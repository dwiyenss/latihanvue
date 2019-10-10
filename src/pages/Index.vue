<template>
  <!-- kiri atas -->
  <q-page class="q-pa-md">
  <!-- tengah center -->
  <!-- clear message tanpa method -->
    <!-- <button @click="message=''">Clear</button> -->
    <!-- clear message dengan method clearMessage -->
    <button @click="clearMessage">Clear</button>
    <!-- textbox -->
    <input v-model="message" @keyup="handleKeyUp"/>
    <H5 v-if=message.length>{{message}}</H5>
    <h6 v-else>No Message</h6>
    <p v-if=message.length>{{ upperCaseMessage() }}</p>
    <h6 v-else>No Uppercase Message</h6>
    <!-- lambang quasar yang ditengah -->
    <img class="q-pa-md-md" alt="Quasar logo" src="~assets/quasar-logo-full.svg">
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
    },
    upperCaseMessage(){
      return this.message.toUpperCase()
    }
  }
  
}
</script>
