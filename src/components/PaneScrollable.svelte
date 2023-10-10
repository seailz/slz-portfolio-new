<!-- Creates two panes, one on the left which is not scrollable, and one on the right which is -->

<div class="panes">
    <div class="not-scrollable">
        <slot name="not-scrollable"></slot>
    </div>

    <div class="scrollable">
        <slot name="scrollable"></slot>
    </div>
</div>

<style>
    .panes {
        display: flex;
        flex-direction: row;
        flex-wrap: nowrap;
        justify-content: flex-start;
        align-items: stretch;
        align-content: stretch;
        height: 100%;
    }

    .scrollable {
        width: 70%;
        overflow-y: scroll;
        scroll-behavior: smooth;
    }

    @media (prefers-reduced-motion: reduce) {
        .scrollable {
            scroll-behavior: auto;
        }
    }

    .scrollable::-webkit-scrollbar {
        width: 0;
        background: transparent; /* make scrollbar transparent */
    }

    .not-scrollable {
        width: 30%;
        overflow-y: hidden;
    }

    .scrollable, .not-scrollable {
        flex: 0 0 auto;
        height: 100%;
    }
</style>