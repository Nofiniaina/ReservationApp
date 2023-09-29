<template>
    <section id="login" class="section-padding border-top">
        <div class="container w-50 h-50 shadow-lg">
            <h1 class="text-center">Sign Up</h1>
            <form @submit.prevent>
                <div class="mb-3">
                    <label for="inputEmail" class="form-label">Email address</label>
                    <input type="email" class="form-control w-50" id="inputEmail" aria-describedby="emailHelp" v-model="email">
                </div>
                <!-- <div class="mb-3">
                    <label for="inputPassword" class="form-label">Password</label>
                    <input type="password" class="form-control w-50" id="inputPassword">
                </div> -->
                <div class="mb-3">
                    <label for="confirmInputPassword" class="form-label"> Confirm password</label>
                    <input type="password" class="form-control w-50" id="confirmInputPassword" v-model="password">
                </div>
                <button type="submit" class="btn btn-primary" @click="login">Submit</button>
                <button type="submit" class="btn btn-primary" @click="seeCurrentUser">See</button>
            </form>
        </div>
    </section>
</template>
<script setup>
    import { ref } from "vue";
    import { supabase } from "../clients/supabase";
    import router from "../router";

    let email = ref("");
    let password = ref("");

    async function createUser() {
        console.log(" you clicked the button");
        const { data, error} = await supabase.auth.signUp({
            email: email.value,
            password: password.value
        });
        if(error) {
            console.log(error);
        } else {
            console.log(data);
            router.push("/");
        }
    }
    async function login(){
        console.log(" you clicked the button");
        const { data, error } = await supabase.auth.signInWithPassword({
            email: email.value,
            password: password.value
        });
        if(error) {
            console.log(error);
        } else {
            console.log(" you clicked the button");
            console.log(data);
            router.push("/about");
        }
    }
    async function seeCurrentUser(){
        const localUser = await supabase.auth.getSession();
        console.log(localUser);
    }
    async function logout(){
        const { error } = await supabase.auth.signOut();
        if(error) {
            console.log(error);
        } else {
            router.push("/");
        }
    }
</script>

<script>
    export default {
        data() {
            return {
                name: 'LoginView',
                email: "",
                password: ""
            }
        }
    }
</script>
<style>

</style>