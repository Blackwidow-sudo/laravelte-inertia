<script>
    let count = 0

    function increment() {
        count++
    }

    function decrement() {
        count--
    }
</script>

<div class="container">
    <span>{count}</span>
    <div>
        <button on:click={decrement}>-</button>
        <button on:click={increment}>+</button>
    </div>
</div>

<style>
    .container {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }
</style>