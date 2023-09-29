<script setup>
import { RouterLink, RouterView } from 'vue-router'

</script>
<script>

</script>
<template>
  <header>
    <div class="wrapper">
      <nav class="navbar navbar-expand-lg bg-body-tertiary fixed-top pt-1 pb-1" >
        <div class="container-fluid">
          <a class="navbar-brand" href="#">
            <img src="./components/icons/nav.png" alt="" width="30" height="24">
            <span>DESTI</span><span>NATION</span>
          </a>
          <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarScroll" aria-controls="navbarScroll" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarScroll">
            <ul class="navbar-nav mx-auto my-2 my-lg-0 navbar-nav-scroll" style="--bs-scroll-height: 100px;">
              <li class="nav-item">
                <RouterLink class="nav-link" to="/">Home</RouterLink>
              </li>
              <li class="nav-item">
                <RouterLink class="nav-link" to="/about">Book place</RouterLink>
              </li>
            </ul>
            <RouterLink class="signin" to="/login">Sign in</RouterLink>
          </div>
        </div>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style>

</style>
<style scoped>

  .navbar container-fluid{
    position: relative;
  }

  .signin{
    padding: 0.75rem 2rem;
    outline: none;
    border: none;
    font-size: 1rem;
    font-weight: 500;
    color: #fff;
    background-color: #4e57d4;
    border-radius: 2rem;
    cursor: pointer;
    transition: 0.3s;
  }

</style>
