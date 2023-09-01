<script lang="ts">
	export let title: string;
	export let link: string;
	export let image: string;
</script>

<a
	href={link}
	target="_blank"
	class="inline-flex ml-2 items-center px-4 py-2 text-sm font-medium text-gray-900 bg-white border border-gray-200 rounded-lg hover:bg-gray-100 hover:text-blue-700 focus:z-10 focus:ring-4 focus:outline-none focus:ring-gray-200 focus:text-blue-700 dark:bg-gray-800 dark:text-gray-400 dark:border-gray-600 dark:hover:text-white dark:hover:bg-gray-700 dark:focus:ring-gray-700"
>
	<img class="mr-2" src={image} alt={title} />
	{title}</a
>
