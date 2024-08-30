<script lang="ts">
    import { weather } from "../stores.ts";

    let weatherValue: number;

    weather.subscribe(value => {
        weatherValue = value;
    });
</script>

<input type="text" placeholder="Set new weather..." bind:value={weatherValue}><br>
<button class="bg-blue-500 p-3 rounded-md text-white" 
on:click={() => weather.set(weatherValue)}>Set weather to {weatherValue}°C</button>