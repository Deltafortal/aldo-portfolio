<script>

    export default {

        data() {
            return {
                
                
            }
        },

    } 


</script>




<template>
   
   <header>

        <!-- Title -->
        <div class="title">
            <i class="bi bi-list d-md-none"></i>
            <h3>AldoLucchetta</h3>
        </div>


        <!-- Navbar -->
        <div class="navbar d-md-block">
            <ul>
                <li><a href="">Home</a></li>
                <li><a href="">Skills</a></li>
                <li><a href="">Projects</a></li>
                <li><a href="">Contacts</a></li>
            </ul>
        </div>

   </header>

</template>




<style scoped lang="scss">

    @use '../assets/scss/vars' as *;

    header {

        height: 15vh;
        padding: 20px;

        display: flex;
        align-items: center;


        .title {
            display: flex;
            align-items: center;


            i {
                transform: translatey(-3px);
            }

        }

        h3 {
            margin-left: 20px;
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
                list-style-type: none;
                margin-right: 40px;
            }

            a {
                text-decoration: none;
                color: white;
                font-size: 18px;
            }

        }

    }
    

    .navbar {
        display: none;
    }


    i {
        font-size: 30px;
    }


</style>