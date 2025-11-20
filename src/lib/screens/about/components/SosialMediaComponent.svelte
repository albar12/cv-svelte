<script lang="ts">
	import { colors } from '$lib';
	import Icon from 'svelte-awesome/components/Icon.svelte';

	export let data;
	export let url: string;
</script>

<a href={url} target="_blank" rel="noopener noreferrer">
	<div class="h-15 w-15 rounded-xl bg-white p-2">
		<Icon {data} class="h-full w-full" style="color: {colors.darkTeal}" />
	</div>
</a>
