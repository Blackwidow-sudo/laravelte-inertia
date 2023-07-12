<script>
    import { inertia, page } from "@inertiajs/svelte";
    import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte'

    export let routes;

    $: isActive = (route) => {
        return $page.url === route;
    }
</script>

<Navbar let:hidden let:toggle>
    <NavBrand href="/">
        <img
            src="https://flowbite-svelte.com/images/flowbite-svelte-icon-logo.svg"
            class="mr-3 h-6 sm:h-9"
            alt="Flowbite Logo"
        />
        <span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white">
            Flowbite
        </span>
    </NavBrand>
    <NavHamburger on:click={toggle} />
    <NavUl {hidden}>
        {#each routes as { name, href }}
            <NavLi active={isActive(href)}>
                <a class="inline-block w-full" {href} use:inertia>{name}</a>
            </NavLi>
        {/each}
    </NavUl>
</Navbar>