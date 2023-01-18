<script lang="ts">
	import TopBar from "$lib/components/TopBar.svelte";
import Title from "../lib/components/Title.svelte";
</script>

<div class="home">
    <div class="content">
        <Title />    
    </div>
    
</div>

<style>
@import url('https://fonts.googleapis.com/css2?family=M+PLUS+2:wght@300&display=swap');
    .home {
        font-family: 'M PLUS 2', sans-serif;
        display: flex;
        width: 100%;
        height: 100%;
        align-items: center;   
        justify-content: center;
    }
    .content {
        top: 50px;
    }
</style>