<script lang="ts">
	import data from '$lib/data/data.json';
	import CustomTimelineItem from './customTimelineItem.svelte';
</script>

<ol class="relative border-l border-gray-200 dark:border-gray-700">
	{#each data.previous_works as work}
		<CustomTimelineItem {...work} />
	{/each}
</ol>
