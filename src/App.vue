
<template>
  <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link :to=" { name:'About' }">About</router-link> |
      <router-link :to="{ name:'Contact' }">Contact</router-link> |
      <router-link :to="{name : 'Jobs'}">Jobs</router-link>

      <br>
      <br>
      <br>

      <button @click="redirect">Redirect</button>
      <button @click="back">Go Back</button>
      <button @click="forward">Forward</button>

     <router-view/>
  </div>
  
</template>
<script>


export default {
  name: 'App',
  components: {
    
  },
  data(){
    return{

    }
  },
  methods: {
     redirect(){
       this.$router.push({name:'Home'})
     },
     back(){
       this.$router.go(-1)
     },
     forward(){
        this.$router.go(1)
     }
  },

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

#nav{
 padding: 10px

}

#nav a{
  padding: 10px;
  text-decoration: none;
  font-weight: bold;
  border-radius: 5px;
 
 }

a.router-link-active.router-link-exact-active {
    background-color: red;
    color: white;
}

button {
    padding: 10px;
    margin: 0 10px;
    border: none;
    cursor: pointer;
}
</style>
