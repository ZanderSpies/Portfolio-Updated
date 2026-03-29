<script setup>
useHead({
  title: "Projects"
})

const username = "ZanderSpies"
const { data: repos, pending, error } = await useFetch(
  `https://api.github.com/users/${username}/repos?sort=updated`,
  {
    transform: (allRepos) => {
      const excludedNames = ['Mechanaut-Vertical', 'Mechanaut-Comic-Book'];
      return allRepos
        .filter(repo => !excludedNames.includes(repo.name))
        .map(repo => ({
          ...repo,
          previewImage: `https://opengraph.githubassets.com/1/${username}/${repo.name}`
        }));
    }
  }
);
</script>


<template>
    <div class="projects-grid">
        <div v-if="pending">
            Loading my latest work...
        </div>

        <div v-else-if="error">
            GitHub is taking a break. Please try again later!
        </div>
        
        <div v-else id="projects-grid">
    <div v-for="repo in repos.slice(0, 6)" :key="repo.id" class="project-card">
        <img :src="`/${repo.name}.png`" alt="Social Preview" id="project-image">
        <p id="heading">{{ repo.name }}</p>
        <div id="card-description">
            <p>{{ repo.description || 'No description provided.' }}</p>
        </div>
        <a :href="repo.html_url" target="_blank" id="view-button">View</a>
    </div>
</div>
    </div>
</template>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Archivo+Black&family=B612:ital,wght@0,400;0,700;1,400;1,700&family=Orbitron:wght@400..900&family=Space+Mono:ital,wght@0,400;0,700;1,400;1,700&display=swap');
    #project-image
    {
        width: 400px;
        height: 250px;
        border-radius: 10px;
    }

    #projects-grid
    {
        display: grid;
        grid-template-columns: auto auto;
        grid-template-rows: auto auto auto;
        justify-content: space-evenly;
        justify-items: center;
    }

    .project-card #heading
    {
        margin: 0;
        margin-bottom: 10px;
        color: #032045;
        font-size: 25px;
        font-weight: 600;
    }

    #card-description p
    {
        margin: 0;
        font-size: 18px;
        color: #95aac7;
        
    }

    .project-card
    {
        margin-bottom: 50px;
        background-color: #366590;
        border-radius: 10px;
        padding: 30px;
        box-shadow: #447cb0 0px 0px 5px 15px;
        font-family: "Orbitron", sans-serif;
        font-optical-sizing: auto;
        font-weight: 400;
        font-style: normal;
    }

    #view-button
    {
        display: block;
        text-align: center;
        margin-top: 10px;
        text-decoration: none;
        color: #a1acbd;
        background-color: #3d4756;
        max-width: 100px;
        margin-left: auto;
        margin-right: auto;
        border-radius: 10px;
        padding: 5px;
    }

    #view-button:hover
    {
        background-color: #29303a;
    }

    

    

    
    
</style>