<script>
		import Info from './Info.svelte';

	const pgk = {
    name: 'svelte',
    version: 3,
    speed: 'blazing',
    website: 'https://svelte.dev',
}
</script>

<Info name={pkg.name} version={pkg.version} speed={pkg.speed} website={pkg.website}/>
