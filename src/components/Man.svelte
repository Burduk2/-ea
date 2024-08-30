<script lang="ts">
    export let name: string;
    export let age: number;
    export let height: number;
    export let weight: number;
</script>

<div class="flex flex-col gap-4 bg-amber-100 w-[300px] p-4 rounded-md mt-10">
    HERE'S A MAN
    <hr>
    <h1>{name}</h1>
    <p>Age: {age}</p>
    <p>Height: {height}</p>
    <p>Weight: {weight}</p>
</div>