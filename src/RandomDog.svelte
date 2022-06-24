<script lang="ts">
    let randomDog = fetchDog();

    async function fetchDog() {
        const res = await fetch("https://dog.ceo/api/breeds/image/random");
        const json = await res.json();
        return json;
    }
</script>

<p>
    <button id="btn" on:click={() => randomDog = fetchDog()}>See random dog</button>
</p>

<section>
    {#await randomDog}
        <p>Loading...</p>
    {:then dog}
        <img id='dog' src={dog.message} alt='dog'/>
    {/await} 
</section>


<style>
    #dog {
        margin-top: 0em;
        height: 65vh;
    }

    button {
        height: 8%;
        font-size: 16px;
        background-color: #a4c2a5;
        color: #ffffff;
        border-color: #ffffff;
    }

    button:hover {
        background-color: #566246;
        border-color: #ffffff;
    }
</style>
