<script>
    import TopNav from "../components/TopNav.svelte";
</script>

<TopNav />

<div class="nav_adjusted">
    <slot></slot>
</div>

<style>
    .nav_adjusted {
        margin-top: 4rem;
        box-sizing: border-box;
        height: calc(100vh - 4rem);
        position: absolute;
        bottom: 0;
    }
</style>