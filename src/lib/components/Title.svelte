<script lang="ts">
    const info = [
    'Information and Communication Technology student at Utu',
    'Co-founder of Kvanttori Oy',
    'passionate about learning to code',
    'kissa ja koira'
]
</script>

<div class="container">
    <a class="name" href="/about">Teemu Salonen</a>
    {#each info as infoLine }
        <h3 class="line">{infoLine}</h3>
    {/each}
</div>

<style>
    @import url('https://fonts.googleapis.com/css2?family=M+PLUS+2:wght@300&display=swap');

    .name {
        text-decoration-line: none;
        font-size: 2em;
        display: flex;
        justify-content: center;
        transform: scale(.9);
        transition: color .5s, transform .5s;
    }
    .name:hover {
        color: rgb(142, 75, 75);
        transform: translateY(-7.5%);
        cursor: pointer;
    }

    .line {
        color: rgb(255, 255, 255);
    }
</style>