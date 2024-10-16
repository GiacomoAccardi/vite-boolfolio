
<script>
export default {
    
}
</script>

<template>
    <header class="bg-white">
        <div class="container">
            <div class="row">
                <div class="col-12 d-flex justify-content-between align-items-center py-4">
                    <h1>Boolfolio <..></h1>
                    <ul class="list-unstyled d-flex mt-3">
                        <li class="me-2"> 
                            <router-link :to="{ name: 'homepage'}">Home</router-link>
                        </li>
                        <li class="me-2"> 
                            <router-link :to="{ name: 'portfolio'}">Portfolio</router-link>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </header>
</template>

<style lang="scss">
    header{
        a{
            text-decoration: none;
            color: rgb(0, 0, 0);

            &:hover{
                font-weight: 700;
                transition: 0.2s;
            }
        }
    }
</style>