<script>
    import { createEventDispatcher } from "svelte";
    const dispatch = createEventDispatcher();

    let name = 'user';
    let checked = false;
</script>

<form action="" class="flex flex-col gap-4 w-full max-w-sm m-auto mt-8">
    <input type="text" placeholder="Username..." 
        class="w-full p-2 border-2 border-gray-300 rounded-md"
        bind:value={name}>
    <input type="password" placeholder="Password..." class="w-full p-2 border-2 border-gray-300 rounded-md">
    
    <div class="flex gap-1">
        <input type="checkbox" id="cbox" bind:checked={checked} class="w-fit">
        <label for="cbox" class="text-sm">Recieve my special pics</label>
    </div>
    
    
    <button class="bg-blue-500 text-white px-4 py-2 rounded-md disabled:bg-blue-300" 
    on:click={() => dispatch('submit')}
    disabled={!checked}>
        Sign in as {name}
    </button>
</form>