<script>

    //Import
    import skills from '../assets/data/logos.js';

    export default {

        data() {
            return {
                
                skills,
                
            }
        },

    } 


</script>




<template>
   
    <section id="skills">

        <div class="content text-center">
            <h2>Le mie competenze</h2>
            <p>
                Queste sono le tecnologie e le competenze che ho acquisito durante il mio percorso. 
                Tutto quello che non c'è, invece, posso impararlo!
            </p>

            <div class="skill-frame">

                <div class="right-frame d-none d-sm-block">
                    <img src="/img/ComputerBoy.jpg" alt="My Avatar">
                </div>

                <div class="skill-logos">
                    <img v-for="skill in this.skills" :src="'/img/logos/' + skill.logo + '-logo.svg'" :alt="skill.logo">
                </div>
            </div>
        </div>

    </section>

</template>




<style scoped lang="scss">

    @use '../assets/scss/vars' as *;


    #skills {
        
        margin-bottom: 200px;

        h2 {

            margin-top: 40px;
            margin-bottom: 50px;

        }

        p {
            margin-bottom: 50px;
        }


        .skill-frame {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 50px;
            flex-basis: 50%;

        }


        .right-frame{

            img {
                width: 90%;
            }
        }

        .skill-logos {
            padding: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-wrap: wrap;
            flex-basis: 100%;
            height: 70vh;
            overflow-y: auto;
            direction: rtl;

            img {
                width: 100px;
                padding: 10px;
            }

            //Scrollbar
            &::-webkit-scrollbar {
                width: 5px;
            }

            &::-webkit-scrollbar-track {
                background: #252525;
            }

            &::-webkit-scrollbar-thumb {
                background: $blue;
            }

            &::-webkit-scrollbar-thumb:hover {
                background: $green;
            }
        }
    }





    /******* Media Queries  *******/



    @media (min-width: 576px) {

        #skills {

        .skill-logos{

            
            img {
                
                width: 95px;
                padding: 8px;
            }
        } 
    }
}




    @media (min-width: 992px) {

    #skills {

        .skill-logos{

            flex-basis: 50%;
            
            img {
                
                width: 120px;
                padding: 15px;
            }
        } 
    }
}




@media (min-width: 1200px) {
    
    #skills {

        .skill-logos{
            
            flex-basis: 50%;

            img {
                
                width: 140px;
                padding: 15px;
            }
        } 
    }
}


</style>