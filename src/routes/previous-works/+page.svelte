<script>
	import CustomTimeline from '$lib/components/timeline/customTimeline.svelte';
	import data from '$lib/data/data.json';
</script>

<svelte:head>
	<title>Previous Works | {data.meta.first_name} {data.meta.last_name}</title>
</svelte:head>

<main class="flex flex-flex justify-center pt-8">
	<CustomTimeline />
</main>
