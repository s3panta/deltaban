<template>
  <v-app>
 
    <Header/>

<Main/>

    <BottomNav/>
  </v-app>
</template>

<script>
import Header from "./components/Header"
import BottomNav from "./components/BottomNav"
import Main from "./Page/Main"
  export default {
    name: 'App',

    components: {
Header,
BottomNav,
Main
    },

   

  }
</script>
<style >
.v-text-field.v-text-field--solo:not(.v-text-field--solo-flat) > .v-input__control > .v-input__slot{
  box-shadow: none !important;
}
</style>