<script>

    export default {
    data() {
        return {
            projects: [
                {
                    id: 1,
                    name: 'BoolBnb',
                    description: 'Riproduzione fedele del famoso sito di AirBnb, realizzato con VueJs per il lato frontend e Laravel per il backend.',
                    image: 'BoolBnb.jpeg',
                },
                {
                    id: 2,
                    name: 'Gobike',
                    description: 'Riproduzione di un sito ecommerce, in questo caso ho preso come riferimento la vendita di corsi per biciclette.',
                    image: 'GoBike.png',
                },
                {
                    id: 3,
                    name: 'BeholderFlix',
                    description: 'Riproduzione di Netflix ispirandosi al famoso mostro di Dungeon and Dragons',
                    image: 'BeholderFlix.png'
                }
                
            ],
            currentIndex: 0,
        };
    },

    methods: {
        showProjectDetails(project) {
        
        console.log('Mostra dettagli del progetto:', project);
        },


        nextProject() {
            this.currentIndex = (this.currentIndex + 1) % this.projects.length;
        },

        prevProject() {
            this.currentIndex = (this.currentIndex - 1 + this.projects.length) % this.projects.length;
        },
        },
    };


</script>




<template>


    <section id="projects">
        <div class="content text-center">

            <div class="title">
                <h2>I Miei Progetti</h2>
                <p>
                    Questi sono alcuni dei progetti che ho realizzato durante il mio percorso. Scorri per vederli tutti!
                </p>
            </div>

            <div class="project-slider">

                <div class="project-container" v-for="(project,i) in projects" v-show="currentIndex === i" :key="project.id">


                    <div class="project-info">
                        <h3>{{ project.name }}</h3>

                        <!-- Figure -->
                        <figure>

                            <div class="arrow left-arrow" @click="prevProject">
                                <i class="bi bi-chevron-left"></i>
                            </div>

                            <img :src="'/img/projects/' + project.image" :alt="project.name" @click="showProjectDetails(project)" />

                            <div class="arrow right-arrow" @click="nextProject">
                                <i class="bi bi-chevron-right"></i>
                            </div>

                        </figure>

                        <p>{{ project.description }}</p>
                    </div>

                </div>
            </div>
        </div>
    </section>

</template>




<style scoped lang="scss">

    @use '../assets/scss/vars' as *;

    #projects {
    margin-bottom: 250px;


    .content {
        display: flex;
        align-items: center;
        flex-direction: column;
    }

    h2 {
        margin-top: 40px;
        margin-bottom: 50px;
    }

    p {
        margin-bottom: 80px;
    }

    .project-slider {
        width: 90%;
        overflow: hidden;
        display: flex;



    figure {
        position: relative;
        width: 100%;
        margin: 0 auto;

        img {
                width: 100%;
                border-radius: 13px;
            }
    }
    
    .arrow {
        display: flex;
        align-items: center;
        justify-content: center;
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        font-size: 2rem;
        z-index: 1;
        background-color: rgba(0, 0, 0, 0.5);
        cursor: pointer;

        &:hover {
            background-color: $green;
        }

        &:active {
            background-color: $green;
        }
    }

    .left-arrow {
      left: 0px;
    }

    .right-arrow {
      right: 0px;
    }


        .project-container {
            flex: 0 0 auto;
            width: 100%;
            transition: transform 0.5s ease-in-out;

            h3 {
                margin-top: 10px;
                margin-bottom: 30px;
            }

            p {
                margin: 0 auto;
                margin-top: 50px;
                margin-bottom: 20px;
                width: 100%;
            }
        }
    }
    }
    
</style>