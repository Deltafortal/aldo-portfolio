<script>

    //Import
    import SkillsSection from './SkillsSection.vue';
    import ProjectsSection from './ProjectsSection.vue';
    import ContactsSection from './ContactsSection.vue';




    export default {

        components: { SkillsSection, ProjectsSection, ContactsSection },

        data() {
            return {
                
                
            }
        },

    } 


</script>




<template>
   
   <main class="container">

       <!-- Skills section -->
       <SkillsSection />
       
       
       <!-- Projects Section-->
       <ProjectsSection />
       
       
       <!-- Contacts -->
       <ContactsSection />
       
    </main>

</template>




<style scoped lang="scss">

    @use '../assets/scss/vars' as *;


    main {
        background-color: $primaryCol;
        
    }

</style>

