<script>
    let greeting = 'Hi'
    let person = 'Shaun'
    let mood = 'excited'

    const handleInput = (e) => {
        mood = e.target.value
    }

    const handleClick = () => {
        mood = 'happy'
    }
</script>

<main>
    <h1>{greeting}, {person}!</h1>
    <p>I am feeling {mood}.</p>
    <!-- <input
        type="text"
        placeholder="How are you feeling?"
        value={mood}
        on:input={handleInput}
    /> -->
    <input type="text" placeholder="How are you feeling?" bind:value={mood} />
    <button on:click={handleClick}>😁</button>
</main>

<style>
    input {
        padding: 14px 10px;
        width: 260px;
        display: inline;
        border: 2px solid #333333;
        border-radius: 6px;
        background-color: #181818;
        transition: 0.2s;
        &:hover {
            border-color: #646cff;
        }
    }
</style>
