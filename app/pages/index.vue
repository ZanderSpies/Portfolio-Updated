<script setup>
/* Zander Spies u25033931 */
import Header from '~/components/header.vue';

useHead({
  title: 'Home'
})

const apiKey = "08d0b8842f51f8cfd57c7a6ff781a6c8"
const { data: weather, pending, error } = await useFetch(`https://api.openweathermap.org/data/2.5/weather?q=Pretoria&units=metric&appid=${apiKey}`)

</script>

<template>
    <div id="description">
        <img src="/profile.jpg" alt="Zander Spies" id="profile">
        <article id="bio">
            <p id="p1">
                I am Zander, a second year Information Science Multimedia student studying at the University of Pretoria.
            </p>

            <p id="p2">
                My studies focus on the development of interactive digital media by combining technology, programming and design.
            </p>

            <p id="p3">
                My main interests lie in programming and software development, particularly building websites and digital applications.
            </p>

            <p id="p4">
                This portfolio features selected projects completed durning my coursework.
            </p>
        </article>
    </div>
    
</template>

<style>
    #bio
    {
        max-width: 650px;
    }

    #description
    {
        display: flex;
        align-items: flex-start;
        justify-content: space-evenly;
    }

    #profile
    {
        height: 450px;
        width: auto;
        margin-bottom: 50px;
    }

    #p1
    {
        margin-top: 0;
    }

    #p4
    {
        margin-bottom: 0;
    }


    .weather-box
    {
    padding: 20px;
    background: rgba(255,255,255,0.1);
    border-radius: 10px;
    text-align: center;
    }

</style>