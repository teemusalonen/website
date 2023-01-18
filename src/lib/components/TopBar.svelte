<script lang="ts">
	import type { Route } from "../types/route";

    const routes: Route[] = [{
        path: 'about',
        text: 'About me'
    }, {
        path: 'contact',
        text: 'Contact'
    },{
        path: '',
        text: 'Home'
    }];
</script>

<div class="topbar">
    {#each routes as route}
        <a class="route" href="/{route.path}">{route.text}</a>
    {/each}
</div>

<style>
    .topbar {
        font-family: 'M PLUS 2', sans-serif;
        display: flex;
        position: absolute;
        justify-content: space-evenly;
        width: 25vw;
    }
    .route {
        text-decoration-line: none;
        font-size: 1.5em;
        justify-content: center;
        color: white;
        transition: text-shadow .4s, transform .4s;
    }
    .route:hover {
        text-shadow: rgba(255, 255, 255, 0.33) 0px 1px 10px;
        transform: translateY(-4%);
    }

</style>