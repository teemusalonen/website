<script lang="ts">
	import TopBar from "$lib/components/TopBar.svelte";
import Title from "../lib/components/Title.svelte";
</script>

<div class="home">
    <div class="topbar">
        <TopBar />
    </div>
    <div class="content">
        <Title />
    </div>
    
</div>

<style>
@import url('https://fonts.googleapis.com/css2?family=M+PLUS+2:wght@300&display=swap');
    .topbar {
        display: flex;
        justify-content: center;
    }

    .home {
        border: solid 1px blue;
        font-family: 'M PLUS 2', sans-serif;

    }
    .content {
        display: flex;
        width: 100%;
        height: 100%;
        margin-top: 50px;
    }
</style>