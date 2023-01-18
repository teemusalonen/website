<script lang="ts">
	import BackButton from "$lib/components/BackButton.svelte";
	import TopBar from "$lib/components/TopBar.svelte";
	import { Aptitude } from "$lib/types/aptitude";
	import type { Technology } from "$lib/types/technology";


    const technologies: Technology[] = [{
        name: 'React', 
        aptitude: Aptitude.Good, 
        info: 'Started learning web development with React. I have completed the Full Stack Course of Helsinki University' 
        }, {
            name:'Angular',
            aptitude: Aptitude.Good
        },{
            name: 'SvelteKit',
            aptitude: Aptitude.SF,
            info: `I've done this project as well as participated in a Junction project using SvelteKit`
        }]
</script>


<div class="about">
    <BackButton />
    <h1 class="header">Skills</h1>
    <div class="content">
        {#each technologies as tech}
            <div class="technology">
                <h2 class="info"> {tech.name}</h2>
                <p class="info">{tech.aptitude}</p>
                <p class="info">{tech.info}</p>
            </div>
            <img alt="eiookuvaa" src="static/favicon.png"> 
        {/each}
    </div>
</div>

<style>
    .about {
        font-weight: 200;
        scroll-behavior: smooth;
        font-family: 'M PLUS 2', sans-serif;
        color: white;
    }
    .header {
        animation: titleFade ease-in 1s;
        font-size: 4em;
        font-weight: 200;
        display: flex;
        justify-content: center;
    }
    
    .content {
        animation: 1s ease-in 0s 1 fadeIn;

        height: 100;
        display: flex;
        align-items: center;
        flex-flow: column;
        justify-content: space-around;
    }

    .technology {
        display: flex;
        flex-direction: column;
        height: 100vh;
    }

    .info {
        
    }

    @keyframes fadeIn {
        0% {
            transform: translateY(.5%);
            opacity: 0;
        }

        100% {
            transform: translateY(0);
            opacity: 1;

        }
    }

    @keyframes titleFade {
        0% {
            transform: translateY(-0%);
            opacity: 0;
        }
        100% {
            transform: translateY(0%);
            opacity: 1;
        }
    }

</style>