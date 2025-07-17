<script lang="ts">
    import MainHeader from "../Components/Layout/Header/MainHeader.svelte";
    import MainFooter from "../Components/Layout/Footer/MainFooter.svelte";
    let { children } = $props();
</script>

<MainHeader />
<main class="flex">
    {@render children()}
</main>
<MainFooter />

<style>
    main {
        padding: 0 var(--container-width-padding);
        margin-top: 53px;

        @media (max-width: 1440px) {
            margin-top: 40px;
        }
        @media (max-width: 1050px) {
            margin-top: 30px;
        }

        @media (max-width: 600px) {
            margin-top: 50px;
        }
    }

</style>
