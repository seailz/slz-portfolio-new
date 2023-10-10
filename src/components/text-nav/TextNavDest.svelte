<script lang="ts">
    import type {Destination} from "../../types/NavTypes";
    import {onMount} from "svelte";

    export let destination:Destination;
    export let onClick:Function = (dest:Destination) => {};

    export function onDestUpdate(dest:Destination) {
        destination = dest;
    }
</script>

<p class="text" class:selected={destination.selected} on:click={() => onClick(destination)}>
        {destination.name}
</p>

<style>
    p {
        color: #878787;
        cursor: pointer;
        transition: color 0.2s ease-in-out;
        margin: 0;
        padding: 1em 0;
    }

    p:hover {
        color: var(--color-text-variant);
    }

    p:active, .selected {
        color: var(--color-text);
    }

    p:before {
        content: "//";
        margin-right: 0.5rem;
        color: #666666;
    }
</style>