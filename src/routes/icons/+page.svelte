
<script lang="ts">
    import { icons } from "../../utils/constansts.ts";
</script>

<div class="flex flex-wrap gap-4 w-full mt-8">
    {#each icons as icon, i}
        <div class="flex flex-col items-center gap-2">
            <img src="/icons/{icon}.svg" alt={icon} class="w-16 max-w-full" />
            <p>Icon #{i}</p>
        </div>
    {/each}
</div>