<script lang="ts">
	import MoreButton from './moreButton.svelte';

	export let title: string;
	export let date: string;
	export let image: string | undefined = undefined;
	export let description: string;
	export let badge: string = '';
	export let more: {
		title: string;
		link: string;
		image: string;
	}[] = [];
</script>

<li class="mb-10 ml-6">
	<!-- image -->
	<span
		class="absolute flex items-center justify-center w-6 h-6 bg-blue-100 rounded-full -left-3 ring-8 ring-white dark:ring-gray-900 dark:bg-blue-900"
	>
		<img src={image} alt={title} class="w-4 h-4 object-contain" />
	</span>
	<!-- title -->
	<h3 class="flex ml-2 mb-1 flex-row items-center font-bold text-2xl">
		{title}
		<span
			class="bg-blue-100 h-fit text-blue-800 text-sm font-medium px-2.5 py-0.5 rounded dark:bg-blue-900 ml-3"
			>{badge}</span
		>
	</h3>
	<time class="block ml-2 mb-2 text-sm font-normal leading-none text-gray-400 dark:text-gray-500"
		>{date}</time
	>
	<p class="mb-4 ml-2 max-w-[85%] md:max-w-md text-base font-normal text-gray-500">
		{description}
	</p>
	{#each more as moreItem}
		<MoreButton {...moreItem} />
	{/each}
</li>
