<script>

    //Import
    import AppHeader from './components/AppHeader.vue';
    import AppJumbotron from './components/AppJumbotron.vue';
    import AppMain from './components/AppMain.vue';



    export default {

        components: { AppHeader, AppJumbotron, AppMain },

        data() {
            return {
                
                
            }
        },

    } 


</script>




<template>
  

    <!-- Header -->
    <AppHeader />


    <!-- Jumbotron -->
    <AppJumbotron />

    
    <!-- Main -->
    <AppMain />


</template>




<style lang="scss">

@use './assets/scss/vars' as *;

body {

    background-color: $black;
    color: white;
}


</style>

