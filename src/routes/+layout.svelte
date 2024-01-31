<script>
    import { page } from "$app/stores";
    import "../app.pcss";
    import logo from "$lib/assets/Palworld-logo.svg";
    import {
        Navbar,
        NavBrand,
        NavLi,
        NavUl,
        NavHamburger,
    } from "flowbite-svelte";
    $: activeUrl = $page.url.pathname;
</script>

<Navbar>
    <NavBrand href="/">
        <img src={logo} class="me-3 h-6 sm:h-9" alt="Palworld Logo" />
        <span
            class="self-center whitespace-nowrap text-xl font-semibold dark:text-white"
            >Palworld 도감 검색</span
        >
    </NavBrand>
    <NavHamburger />
    <NavUl {activeUrl}>
        <NavLi href="/">Home</NavLi>
        <NavLi href="/search">도감 검색</NavLi>
    </NavUl>
</Navbar>
