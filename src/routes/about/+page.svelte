<script lang="ts">
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
    {#each technologies as tech}
        <div class="technology">
            <p class="info">{tech.name}</p>
            <p>{tech.aptitude}</p>
            <p>{tech.info}</p>
        </div>
    {/each}
</div>

<style>
    .about {
        font-family: 'M PLUS 2', sans-serif;
        height: 100;
        display: flex;
        align-items: center;
        flex-flow: column;
        justify-content: space-around;
        margin-top: 100px;
        color: white;
    }

    .technology {
        justify-content: space-between;
    }

    .info {
        float: left;
    }
</style>