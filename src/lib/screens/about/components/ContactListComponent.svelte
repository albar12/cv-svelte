<script lang="ts">
	import { colors } from '$lib';
	import Icon from 'svelte-awesome/components/Icon.svelte';

	export let data;
	export let title: string;
	export let desc: string;
</script>

<div class="mt-8 flex items-center gap-4">
	<div class="h-15 w-15 rounded-xl bg-white p-2">
		<Icon {data} class="h-full w-full" style="color: {colors.darkTeal}" />
	</div>

	<div class="flex flex-col text-white">
		<div class="text-xl">{title}</div>
		<div class="text-lg">{desc}</div>
	</div>
</div>
