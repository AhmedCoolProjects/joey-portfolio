<script>
	import { Timeline, Button } from 'flowbite-svelte';
	import CustomTimelineItem from './customTimelineItem.svelte';
	import data from '$lib/data/data.json';
</script>

<Timeline order="vertical">
	{#each data.previous_works as work}
		<CustomTimelineItem title={work.title} date={work.date} description={work.description}>
			{#if work.more}
				<Button color="alternative">
					{work.more}
				</Button>
			{/if}
		</CustomTimelineItem>
	{/each}
</Timeline>
