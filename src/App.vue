  
<template>
<v-app id="app">
   <NavBar> </NavBar>
   <v-content>
     <v-container>
        <Home></Home>
     </v-container>
   </v-content>
</v-app>
</template>

<script>
import NavBar from './components/NavBar.vue'
import Home from   './pages/Home.vue'
export default {
  name: 'App',
  components: {
    NavBar,
    Home,
  }
}
</script>

<style>
#app{
  background-color: #eae6e6;
  
}
</style>