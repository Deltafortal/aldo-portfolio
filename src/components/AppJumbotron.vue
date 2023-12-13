<script>

    export default {

        data() {
            return {
                
                
            }
        },

    } 


</script>




<template>
   
   <section id="jumbotron" class="container">

        <div class="content">
            <div class="title">
                <h1>Aldo Lucchetta</h1>
                <h3 class="text-center">Full Stack Web Developer</h3>
            </div>
            <div class="sun">
            </div>
        </div>
   </section>

</template>




<style scoped lang="scss">

    @use '../assets/scss/vars' as *;


    #jumbotron {

        height: 90vh;
        padding-bottom: 70px;
        
        h3 {
            margin-top: 50px;

        }

        .content {
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;
            width: 100%;
            height: 100%;

            /*.title {
                background-color: rgba(0, 0, 0, 0.5);
                padding: 150px;
                border-radius: 20px;
            } */
        }

        .sun {
            position: absolute;
            top: 50px;
            right: 35px;
            width: 150px;
            height: 150px;
            background-color: $blue;
            border-radius: 50%;
            box-shadow: 0 0 20px $blue;
            animation: shine 4s ease-in-out infinite;
        }
    }    


    @keyframes shine {

        50%{
            box-shadow: 
                0 0 60px $blue,
                0 0 150px $blue;
        }
    }

</style>