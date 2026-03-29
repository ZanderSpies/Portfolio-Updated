<script setup>
/*Zander Spies u25033931*/
</script>

<template>
  <div id="back-layer">
    <navbar />
    <div id="front-layer">
    
    <Header />
    <NuxtPage />
    <NuxtRouteAnnouncer />
    </div>
  </div>
  
</template>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Archivo+Black&family=B612:ital,wght@0,400;0,700;1,400;1,700&family=Orbitron:wght@400..900&display=swap');
  body
  {
    margin: 0;
    font-family: "Archivo Black", sans-serif;
    font-weight: 400;
    font-style: normal;
    
    background-color: #21374f;
    color: #b0b4b7;
  }

  #front-layer
    {
        margin-left: 150px;
        margin-right: 150px;
        margin-top: 20px;
        margin-bottom: 50px;
        background-color: #366590;
        box-shadow: 10px 10px 10px 10px black;
        font-size: 20px;
    }
</style>
