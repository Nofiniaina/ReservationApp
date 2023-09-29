<template>
    <section id="hero" class="min-vh-100 d-flex align-items-center text-center">
        <div class="container">
            <div class="row">
                <div class="col-12">
                    <h1 data-aos="fade-left" class="text-uppercase text-white fw-semibold display-1">Welcome to Destination</h1>
                    <h5 class="text-white mt-3 mb-4" data-aos="fade-right">BOOK YOUR CAR TICKET PLACE EVERYWHERE</h5>
                    <div data-aos="fade-up" data-aos-delay="50">
                        <a href="#" class="btn btn-brand me-2">Start booking</a>
                        <a hr  ef="#" class="btn btn-light ms-2">Our Portfolio</a>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
    export default{
        data(){
            return{
                name : "HeroContent"
            }
        }
    }
    
</script>
<style>
    #hero{
        background: linear-gradient(rgba(0, 247, 237, 0.3), rgba(159, 176, 179, 0.8)), url(../../assets/images/hero-bg.jpg);
        background-size: cover;
        background-position: center;
    }
</style>