<script>

    export default {

        data() {
            return {
                
                visibility: false
            }
        },

        methods: {

            toggleMenu() {
                console.log("hey");
                this.visibility = !this.visibility
            }
        }

    } 


</script>




<template>
   
   <header>

    <!-- Hamburgher Nav-->
    <div class="hamburgher-nav">

    </div>


        <div class="hamburgher-nav d-md-none" :data-visible="this.visibility">
            <ul>
                <div class="toggle" @click="toggleMenu"><i class="bi bi-list d-md-none"></i></div>
                <li><a href="#jumbotron" aria-hidden="true">00 <span>Home</span></a></li>
                <li><a href="#skills" aria-hidden="true">01 <span>Skills</span></a></li>
                <li><a href="#projects" aria-hidden="true">02 <span>Projects</span></a></li>
                <li><a href="#contacts" aria-hidden="true">03 <span>Contacts</span></a></li>
            </ul>
        </div>

        <!-- Title -->
        <div class="title">
            <i class="bi bi-list d-md-none" @click="toggleMenu"></i>
            <h3>
               <a href="/">AldoLucchetta</a>
            </h3>
        </div>


        <!-- Navbar -->
        <div class="navbar d-md-block">
            <ul>
                <li><a href="#jumbotron" aria-hidden="true"><span>Home</span></a></li>
                <li><a href="#skills" aria-hidden="true"><span>Skills</span></a></li>
                <li><a href="#projects" aria-hidden="true"><span>Projects</span></a></li>
                <li><a href="#contacts" aria-hidden="true"><span>Contacts</span></a></li>
            </ul>
        </div>

   </header>

</template>




<style scoped lang="scss">

    @use '../assets/scss/vars' as *;

    header {

        height: 10vh;
        padding: 20px;

        display: flex;
        align-items: center;


        .title {
            display: flex;
            align-items: center;

            a {
                color: $green;

                &:hover {
                    color: $blue;
                }
            }

            i {
                transform: translatey(-3px);
            }

        }

        h3 {
            margin-left: 20px;

            a {
                font-size: 40px;
            }
        }

        .navbar {
            margin: 0 auto;
            transform: translateY(4px);

            ul {
                display: flex;
                align-items: center;
                justify-content: center;
            }

            li {
                margin-right: 40px;
            }

        }


        a {
                color: $blue;
                font-size: 18px;

                &:hover {
                    color: $green;
                }
            }

        .hamburgher-nav {
            position: fixed;
            inset: 0 60% 0 0;
            z-index: 2;
            background-color: $darkBlack;

            transform: translateX(-100%);
            transition: transform 350ms ease-out;

            padding: 20px 10px;

            li {
                margin-bottom: 25px;
            }

            .toggle {
                margin-bottom: 40px;
                text-align: end;
                padding-right: 10px;
            }
        }


        .hamburgher-nav[data-visible="true"] {
            transform: translateX(0%);
        }

    }
    

    .navbar {
        display: none;
    }


    i {
        font-size: 30px;
    }




    @supports (backdrop-filter: blur(20px)) {
        
        header {

            .hamburgher-nav {
                
                background: hsl(0 0% 30% / 0.1);
                backdrop-filter: blur(20px);
            }
        }
    }



    @media (min-width: 768px) {

        header {

            .hamburgher-nav {
                background: none;
                backdrop-filter: none;
            }
        }
    }

</style>