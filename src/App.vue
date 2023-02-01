<template>
  <div>
    <Title :titleText="text" :text="text2"/>
    <Button @clean="cleanInput"/>
    <!-- Clean eventini @ şeklinde çağırdım. -->
    <input type="text" ref="inputText">
  </div>
</template>

<script>
import Title from './components/Title1.vue'//Component'i buraya ekledim burada kullancağımı söyledim.
import Button from './components/Button.vue'
export default {
  name: 'App',
  components:{
    Title,
    Button
  },
  data(){
    return{
      text:"Vue 3'e Giriş",
      text2:"Vue'ye hoş geldiniz!!"
      //Buradaki props üzerinden beslenmesi için :titleText'i v-bind ettik
    }
  },
  methods:{
    cleanInput(){
      this.$refs.inputText.value = '';
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
