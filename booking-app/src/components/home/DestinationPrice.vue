<template>
    <section id="pricing">
        <div class="container">
            <div class="row">
                <div class="col-12 text-center" data-aos="fade-down" data-aos-delay="150">
                    <div class="section-title">
                        <h1 class="display-4 fw-semibold">Pricing</h1>
                        <div class="line"></div>
                    </div>
                </div>
                <div class="row text-center justify-content-center">
                    <div>
                        <div class="justify-content-center">
                            <label for="">Departure</label>
                            <Dropdown v-model="selectedCityDep" editable :options="cities" optionLabel="city" placeholder="Select a City" class="m-3 w-full md:w-14rem" />
                            <label class="m-3" for="">Arrival</label>
                            <Dropdown v-model="selectedCityArr" editable :options="cities" optionLabel="city" placeholder="Select a City" class="w-full md:w-14rem" />
                            <button class="m-3 btn btn-primary" @click="change">View</button>
                        </div>
                    </div>
                </div>
                <div class="col-lg-4 mb-5 mb-lg-0" data-aos="fade-down" data-aos-delay="250">
                    <div class=" h-100 w-100 bg-white p-5 rounded-lg shadow text-center">
                        <h1 class="font-weight-bold mb-4">VIP</h1>
                        <h2 class="font-weight-bold">COUCOU<span></span></h2>
                        <div class="custom-separator my-4 mx-4 bg-primary"></div>
                    </div> 
                </div>
                <div class="col-lg-4 mb-5 mb-lg-0" data-aos="fade-down" data-aos-delay="350">
                    <div class=" h-100 w-100 bg-white p-5 rounded-lg shadow text-center">
                        <h1 class="font-weight-bold mb-4">VIP</h1>
                        <h2 class="font-weight-bold">COUCOU<span></span></h2>
                        <div class="custom-separator my-4 mx-4 bg-primary"></div>
                    </div> 
                </div>
                <div class="col-lg-4 mb-5 mb-lg-0" data-aos="fade-down" data-aos-delay="450">
                    <div class=" h-100 w-100 bg-white p-5 rounded-lg shadow text-center">
                        <h1 class="font-weight-bold mb-4 ">VIP</h1>
                        <h2 class="font-weight-bold">PRICE</h2>
                        <div class="custom-separator my-4 mx-4 bg-primary"></div>
                        <ul class="list-unstyled my-5 text-left">
                            <li class="mb-3"></li>
                        </ul>

                    </div> 
                </div>
            </div>
        </div>
    </section>            
</template>
<script>
    import Dropdown from 'primevue/dropdown';
    export default {
        data() {
            return {
                name: 'DestinationPrice',
                selectedCityDep: null,
                selectedCityArr: null,
                cities: [
                    {city : 'Antananarivo'},
                    {city : 'Antsirabe'},
                    {city : 'Fianarantsoa'},
                    {city : 'Morondava'},
                    {city : 'Toliara'},
                    {city : 'Mahajanga'},
                    {city : 'Antsiranana'},
                    {city : 'Toamasina'}
                ]
            };
        },
        methods : {
            change(){
                alert('view');
                console.log(" you clicked the button");
            }
        },
        components: {
            Dropdown
        }
    }
</script>
<style scoped>

</style>