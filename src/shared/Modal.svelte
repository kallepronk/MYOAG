<script>
    export let showModal = false;
</script>

{#if showModal}
    <div class="w-full h-full backdrop-blur bg-opacity-50 bg-black fixed top-0 left-0 grid content-center" on:click|self>
        <div class="p-4 rounded-2xl max-w-xl bg-white text-center m-auto">
            <slot name="title"></slot>
            <slot></slot>
        </div>
    </div>
{/if}