<script>
	import { writable } from 'svelte/store';
    export const count = writable(0);

	// import Incrementer from './Incrementer.svelte';
	// import Decrementer from './Decrementer.svelte';
	// import Resetter from './Resetter.svelte';

	let countValue;

	count.subscribe(value => {
		countValue = value;
	});

    const handleclick = () => {
        count.update((n) => {
            return n + 1;
        });
    }
</script>

<h1>The count is {countValue}</h1>

<button on:click={handleclick}>Increment</button>
<button on:click={() => count.update((n) => {
    return n - 1;
})}>Decrement</button>