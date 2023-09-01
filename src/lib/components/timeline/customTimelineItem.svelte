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
	} = {
		title: '',
		link: ''
	};
</script>

<li class="mb-10 ml-6">
	<span
		class="absolute flex items-center justify-center w-6 h-6 bg-blue-100 rounded-full -left-3 ring-8 ring-white dark:ring-gray-900 dark:bg-blue-900"
	>
		<svg
			class="w-2.5 h-2.5 text-blue-800 dark:text-blue-300"
			aria-hidden="true"
			xmlns="http://www.w3.org/2000/svg"
			fill="currentColor"
			viewBox="0 0 20 20"
		>
			<path
				d="M20 4a2 2 0 0 0-2-2h-2V1a1 1 0 0 0-2 0v1h-3V1a1 1 0 0 0-2 0v1H6V1a1 1 0 0 0-2 0v1H2a2 2 0 0 0-2 2v2h20V4ZM0 18a2 2 0 0 0 2 2h16a2 2 0 0 0 2-2V8H0v10Zm5-8h10a1 1 0 0 1 0 2H5a1 1 0 0 1 0-2Z"
			/>
		</svg>
	</span>
	<h3 class="flex items-center mb-1 text-lg font-semibold text-gray-900 dark:text-white">
		{title}
		<span
			class="bg-blue-100 text-blue-800 text-sm font-medium mr-2 px-2.5 py-0.5 rounded dark:bg-blue-900 dark:text-blue-300 ml-3"
			>{badge}</span
		>
	</h3>
	<time class="block mb-2 text-sm font-normal leading-none text-gray-400 dark:text-gray-500"
		>{date}</time
	>
	<p class="mb-4 text-base font-normal text-gray-500 dark:text-gray-400">
		{description}
	</p>
	{#if more.title !== ''}
		<MoreButton {...more} />
	{/if}
</li>
