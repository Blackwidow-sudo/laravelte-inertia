<script context="module">
    export { default as layout } from './Layout.svelte';
</script>

<script>
    import Counter from '../Components/Counter.svelte'

    export let name
</script>

<h1>Hello {name}</h1>
<Counter />
