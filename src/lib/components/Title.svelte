<script lang="ts">
    const info = [
    'Information and Communication Technology student at Utu',
    'Co-founder of Kvanttori Oy',
    'passionate csgo player'
]
</script>

<div class="title">
    <a class="name" href="/about">Teemu Salonen</a>
    <div class="line-container">
        {#each info as infoLine }
            <h3 class="line" style="fontStyle: {infoLine.includes('csgo') ? 'italic': ''}">{infoLine}</h3>
        {/each}
    </div>
   
</div>

<style>
    @import url('https://fonts.googleapis.com/css2?family=M+PLUS+2:wght@300&display=swap');

    .title {
        border: solid 1px red;
        float: left;
        width: 50vw;
        margin-top: 20vh;
    }

    .name {
        color: rgb(171, 171, 171);
        text-decoration-line: none;
        font-size: 1.9em;
        display: flex;
        justify-content: center;
        transform: scale(.975);
        transition: color .5s, transform .5s;
    }
    .name:hover {
        color: rgb(255, 255, 255);
        transform: translateY(-5%);
        cursor: pointer;
    }

    .line-container {
        display: flex;
        flex-direction: column;
    }

    .line {
        font-size: .8em;
        color: rgb(171, 171, 171);

        
        margin: 5px;
        display: flex;
        justify-content: center;
    }
</style>