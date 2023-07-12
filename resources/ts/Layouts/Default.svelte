<script>
    import { inertia, router } from '@inertiajs/svelte'
    import Navbar from '../Components/Navbar.svelte';

    const routes = [
        { name: 'Home', href: '/' },
        { name: 'About', href: '/about' },
        { name: 'Contact', href: '/contact' },
        { name: 'Register', href: '/register' },
        { name: 'Login', href: '/login' },
    ]

    function onLogout() {
        router.get('/logout')
    }
</script>

<header>
    <Navbar {routes} />
</header>
<main class="container mx-auto">
    <slot />
</main>
