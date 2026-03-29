<script setup>
/* Zander Spies u25033931 */
</script>

<template>
    
    <div id="container">
        <ul id="nav">
            <li><NuxtLink to="/">Home</NuxtLink></li>
            <li><NuxtLink to="/projects">Projects</NuxtLink></li>
            <li><NuxtLink to="/contact">Contact</NuxtLink></li>
        </ul>
    </div>
</template>

<style>
    #nav li
    {
        list-style: none;
        display: inline;
        padding: 10px;
        
    }

    #container
    {
        display: flex;
        justify-content: center;
        margin: 0;
        margin-top: 20px;
        font-size: 30px;
    }

    #nav a
    {
        text-decoration: none;
        color: #b0b4b7;
    }

    #nav
    {
        padding: 0;
    }

    .router-link-exact-active
    {
        background-color: #4d88acb5 !important;   
        border-radius: 25px;
        padding: 5px;
        box-shadow: #4d88acdc 0px 0px 40px 10px;
    }
</style>