<script>

    export default {

        data() {
            return {
                
                
            }
        },

    } 


</script>




<template>
   
   <section id="contacts">

        <div class="content container">

            <!-- Left content-->
            <div class="left-content">

                <div class="title">
                    <h3>Aperto a tutte le opportunità</h3>
                    <p>
                        Hai una proposta per me? sono pronto ad ascoltarla!
                        inviami pure un'email oppure un messaggio.
                    </p>
                </div>

                <div class="contacts-side">
                    <h4>Contattami qui:</h4>
                    <ul>
                        <li>
                            <h5>
                                <a href="mailto: aldolucchetta21@gmail.com">
                                    aldolucchetta21@gmail.com
                                </a>
                            </h5>
                        </li>
                        <li>
                            <a href="https://www.linkedin.com/in/aldo-lucchetta-23b560292/">
                                Linkedin
                            </a>
                        </li>
                        <li>
                            <a href="https://github.com/Deltafortal">
                                Github
                            </a>
                        </li>
                        
                    </ul>

                </div>

            </div>

            <!-- Right content-->
            <div class="right-content d-md-flex">

                <figure>
                    <!-- <img src="/img/me.png" alt="Me"> -->
                </figure>

                <div class="interest text-center">
                    <h4>I miei interessi personali</h4>
                    <ul>
                        <li>Intelligenza Artificiale e Machine Learning</li>
                        <li>Frontend Development con VueJS</li>
                        <li>Backend Development con Java</li>
                        <li>C++ e altri linguaggi di programmazione</li>
                        <li>Videogames Development come passatempo</li>
                    </ul>
                </div>
            </div>
        
        </div>


    </section>

</template>




<style scoped lang="scss">

    @use '../assets/scss/vars' as *;


    #contacts {

        background-color: $darkBlack;
        padding: 20px;

        .content {

            height: 100%;
            display: flex;
            justify-content: center;

            h3 {
                font-size: 35px;
            }

            p {
                margin-top: 35px;
                font-size: 18px;
            }

            ul {
                padding-left: 0px;
            }
        }

        .left-content, .right-content {
            padding: 10px;
        }


        /* Left Content */
        .left-content {
            flex-basis: 60%;
            display: flex;
            flex-direction: column;
            justify-content: space-around;

        }

        .contacts-side {

            li {
                margin-bottom: 20px;
            }

            a {
                font-size: 20px;
                color: white;
            }

            h5 {

                a {
                    font-size: 24px;
                    text-decoration: underline;
                    text-decoration-thickness: 5px;
                    text-decoration-color: $green;
                }
            }

            h4 {
                margin-bottom: 40px;
                color: $blue;
            }

        }


        /* Right Content */
        .right-content {
            flex-basis: 40%;
            background-color: $black;
            display: flex;
            flex-direction: column;
            justify-content: flex-start;
            align-items: center;
            display: none;
            box-shadow: 0 0 5px 5px $black;

            figure {
                width: 200px;
                height: 200px;
                border-radius: 50%;
                box-shadow: 
                    0 0 5px 5px $black,
                    0 0 10px 5px $blue,
                    0 0 10px 5px $green;

                display: flex;
                align-items: center;
                justify-content: center;
                background-image: url("./img/me.png");
                background-size: cover;
                background-position-x: -25px;
            }
        }

        .interest {
            margin-top: 40px;

            h4 {
                font-size: 28px;
                margin-bottom: 40px;
                color: $green;
            }

            li {
                margin-bottom: 12px;
                color: white;

            }
        }
    }
    




    /********* MEDIA QUERY **********/
    @media (min-width: 992px) {
    #contacts {

        .right-content {

            figure {
                width: 250px;
                height: 250px;
            }
        }
    }
}

</style>