<script>
    export let description = "this is not the description you are looking for!";
    export let input = "";
</script>

<label class="block w-full mb-4"> {description}
    <textarea class="p-1 border-black block border-2 rounded-lg w-full" bind:value={input} required></textarea>
</label>
