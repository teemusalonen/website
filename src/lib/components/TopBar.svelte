<script lang="ts">
	import type { Route } from "../types/route";

    const routes: Route[] = [{
        path: '',
        text: 'Home'
    },{
        path: 'about',
        text: 'About me'
    }, {
        path: 'contact',
        text: 'Contact'
    }];
</script>

<div class="topbar">
    <div class="routes">
        {#each routes as route}
            <a class="route" href="/{route.path}">{route.text}</a>
        {/each}
    </div>
    <div>
        <input class="search-input" placeholder="looking for a specific thing?"/>
        <img class="search-icon" alt="search" src="src/lib/images/search.png">
    </div>
</div>

<style>
    .topbar {
        border: solid 1px violet;
        font-family: 'M PLUS 2', sans-serif;
        
        display: flex;
        justify-content: space-between;
        position: absolute;
        align-items: center;
        
        width: 97.5vw;
        height: 50px;
    }

    .routes {
        border: solid 1px green;
        display: flex;
        width: 20vw;
        justify-content: space-between;
    }
    .route {
        text-decoration-line: none;
        font-size: 1.5em;
        justify-content: center;
        color: rgb(134, 134, 134);
        transition: color .4s, transform .4s;
    }
    .route:hover {
        color: white;
        transform: translateY(-4%);
    }

    .search-input {
        margin-top: 10px;
        padding: 5px;
        background: none;
        border: none;
        color: aliceblue;
        border-bottom: solid rgba(0, 0, 0, 0) 1px;
    }

    .search-input:focus {
        transition: border-bottom .5s;
        border-bottom: solid 1px white;
        outline: none;
    }

    .search-icon {
        transform: scale(.33);
        top: -20px;
        right: -20px;
        position: fixed;
    }
</style>