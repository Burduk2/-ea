<script lang="ts">
    export let username: null | string = null;
    import { weather } from "../routes/stores.ts";
</script>

<nav class="flex justify-between p-6 border-b-2 border-gray-700">
    <div class="flex gap-4">
        <a href="/" class="hover:text-blue-500">Home</a>
        <a href="/icons" class="hover:text-blue-500">Icons</a>
        <a href="/generator" class="hover:text-blue-500">Generator</a>
        <a href="/weather" class="hover:text-blue-500">Weather</a>
    </div>
    <div class="flex gap-4">
        {#if username}
            <button>{username}</button>
        {:else}
            <a href="/signin" class="hover:text-blue-500">Sign in</a>
        {/if}

        <div>{$weather}°C</div>
    </div>
    
</nav>