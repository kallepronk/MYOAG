<script>
    import "../app.css";
</script>

<div class="grid grid-cols-4 bg-amber-950 h-screen">
    <div class="col-span-1">
    </div>
    <div class="bg-white col-span-2 p-5">
        <slot />
    </div>
    <div class="col-span-1">
    </div>
</div>
