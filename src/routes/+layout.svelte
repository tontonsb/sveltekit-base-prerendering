<script>
    import {page} from '$app/stores'

    $: lang = $page.params.lang ?? 'en'
</script>

<svelte:head>
    <base href="/{lang}/">
</svelte:head>

<nav>
    <a href="/{lang}">Index</a>
    <a href="section">Section</a>
</nav>

<slot />

<style>
    nav {
        display: flex;
        gap: 1rem;
    }
</style>