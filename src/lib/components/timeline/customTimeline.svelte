<script lang="ts">
	import data from '$lib/data/data.json';
	import CustomTimelineItem from './customTimelineItem.svelte';
</script>

<ol class="relative border-l max-w-[85%] border-blue-300">
	{#each data.previous_works as work}
		<CustomTimelineItem {...work} />
	{/each}
</ol>
