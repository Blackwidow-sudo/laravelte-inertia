<script context="module">
</script>

<script lang="ts">
    import Counter from '../Components/Counter.svelte'

    export let name: string
</script>

<h1>Hello {name}</h1>
<Counter />
