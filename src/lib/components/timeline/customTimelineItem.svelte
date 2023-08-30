<script lang="ts">
	import { TimelineItem } from 'flowbite-svelte';
	import { Icon } from 'flowbite-svelte-icons';
	export let title: string;
	export let date: string;
	export let description: string;
</script>

<TimelineItem {title} {date}>
	<svelte:fragment slot="icon">
		<span
			class="flex absolute -left-3 justify-center items-center w-6 h-6 bg-primary-200 rounded-full ring-8 ring-white dark:ring-gray-900 dark:bg-primary-900"
		>
			<img src="/favicon.png" class="w-3 h-3 text-primary-600 dark:text-primary-400" />
		</span>
	</svelte:fragment>
	<p class="text-base font-normal text-gray-500 dark:text-gray-400">
		{description}
	</p>
	<slot />
</TimelineItem>
