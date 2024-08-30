
<script>
    import { generateIcon } from "../../utils/generateIcon.ts";

    let promise = generateIcon();
</script>

<button class="bg-blue-500 text-white px-4 py-2 rounded-md hover:bg-blue-600 mb-8"
on:click={() => { promise = generateIcon() }}>
    Generate an icon
</button>

{#await promise}
    <p>Generating an icon...</p>
{:then icon}
    <img src="/icons/{icon}.svg" alt={icon} class="w-32 max-w-full" />
{:catch err}
    <p class="text-red-500">{err}</p>
{/await}