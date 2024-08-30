<script>
	import Form from "./Form.svelte";
    
    let signedIn = false;
</script>



<h1 class="text-center text-3xl font-bold mt-12">Sign in</h1>

<Form on:submit={() => { signedIn = true }} />

{#if signedIn}
    <p class="text-center text-xl mt-8">You're signed in!</p>
{/if}