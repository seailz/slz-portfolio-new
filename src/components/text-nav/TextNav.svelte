<script lang="ts">
    import type {Destination} from "../../types/NavTypes";
    import TextNavDest from "./TextNavDest.svelte";

    export let destinations:Destination[];

    function onDestinationClick(dest:Destination) {
        destinations.forEach(d => d.selected = false);
        dest.selected = true;
        destinations = destinations;
        window.location.href = dest.path;
    }
</script>

<div class="text-nav">
    {#each destinations as dest}
        <TextNavDest destination={dest} onClick={onDestinationClick} />
    {/each}
</div>

<style>
    .text-nav {
        display: flex;
        flex-direction: column;
    }
</style>