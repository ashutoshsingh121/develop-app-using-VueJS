<template>
  <img alt="Vue logo" src="./assets/logo.png">
  
  <form @submit.prevent="onSubmit">
  <div class="form-group">
    <label for="string">Enter Any String</label><br>
    <input type="text" id="string" class="form-control" v-model="data.string"><br>
    <button type="submit">Click Me</button>
  </div>
  </form>
  <br>
  <StringForm :msg="data.str"/>
</template>

<script>
import StringForm from './components/StringForm.vue'

export default {
  name: 'App',
  components: {
    StringForm
  },
  data() {
    return {
        data: {
            string: '',
            str: ''
        }
    }
  },
  methods:{
    onSubmit(){
      this.data.str=this.data.string.toUpperCase();
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
