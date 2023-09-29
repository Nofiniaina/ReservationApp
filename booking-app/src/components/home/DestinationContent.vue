<template>
    <section id="destination" class="section-padding border-top">
        <div class="container">
            <div class="row">
                <div class="col-12 text-center">
                    <div class="section-title">
                        <h1 class="display-4 fw-semibold">Avalaible destination</h1>
                        <div class="line"></div>
                        <p>we love to travel with you and give you an exceptional experience with our services</p>
                    </div>
                </div>
            </div>
            <div class="row g-4 text-center justify-content-center">
                <div v-for="(avalaible, indexdest) in avalaibles" class="col-lg-4 col-sm-6" :key="indexdest">
                    <div class="city shadow p-lg-5 p-4" :id="avalaible.city">                        
                        <h5 class="mt-4 mb-3">{{ avalaible.city }}</h5>
                    </div>
                </div> 
            </div>
        </div>
    </section>
</template>
<script>
    export default{
        data(){
            return {
                avalaibles : [
                    {city : 'Antananarivo'},
                    {city : 'Antsirabe'},
                    {city : 'Fianarantsoa'},
                    {city : 'Morondava'},
                    {city : 'Toliara'},
                    {city : 'Mahajanga'},
                    {city : 'Antsiranana'},
                    {city : 'Toamasina'}
                ],
                name : 'DestinationContent'
            } 
        }  
       
    }
</script>
<style>

    .city {
        position: relative;
        overflow: hidden;
        z-index: 2;
    }

    .city::after {
        content: "";
        width: 40px;
        height: 40px;
        /* background: rgba(var(--c-brand-rgb), 0.2); */
        position: absolute;
        bottom: 0;
        right: 0;
        transition: var(--transition);
    }


    .city:hover::after {
        width: 100%;
        height: 100%;
        z-index: -1;
    }
    #Antananarivo:hover::after {
        background: url(../../assets/images/city/tana.jpg) center/cover;
    }
    #Antsirabe:hover::after {
        background: url(../../assets/images/city/bira.jpg) center/cover;
    }
    #Fianarantsoa:hover::after {
        background: url(../../assets/images/city/fianara.jpg) center/cover;
    }
    #Toliara:hover::after {
        background: url(../../assets/images/city/toliara.jpg) center/cover;
    }
    #Mahajanga:hover::after {
        background: url(../../assets/images/city/mahajanga.jpg) center/cover;
    }
    #Antsiranana:hover::after {
        background: url(../../assets/images/city/antsiranana.jpg) center/cover;
    }
    #Toamasina:hover::after {
        background: url(../../assets/images/city/toamasina.jpg) center/cover;
    }
    #Morondava:hover::after {
        background: url(../../assets/images/city/morondava.jpg) center/cover;
    }

    .city:hover h5{
        color: white;
    }

    .city:hover .iconbox {
        background-color: rgba(255,255,255,0.2);
        /* color: white; */
    }

</style>