<script lang="ts">
	import '../app.css';
	import favicon from '$lib/assets/favicon.svg';
	import { SvelteToast } from '@zerodevx/svelte-toast';
	import { MainLayout, Footer } from '$lib';

	let { children } = $props();
</script>

<SvelteToast />
<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<MainLayout>
	{@render children()}
	<Footer />
</MainLayout>
