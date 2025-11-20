<script lang="ts">
	export let title: string;
	export let desc: string;
	export let src: string;
	export let srcMobileMode: string;
	export let url: string;
	export let isApk = false;

	let show = false;
</script>

<button
	class="flex w-[175px] shrink-0 flex-col items-center justify-center gap-4 md:w-[350px]"
	on:click={() => (show = true)}
>
	<div
		class="flex h-[125px] w-full items-center justify-center overflow-hidden rounded-xl md:h-[250px]"
	>
		<img {src} alt={title} class="h-full w-full object-cover" />
	</div>
	<div class="text-center text-sm font-medium text-pretty text-white lg:text-2xl">
		{title}
	</div>
</button>

<!-- untuk modal detail -->
{#if show}
	<div class="fixed inset-0 flex items-center justify-center bg-black/30 px-4">
		<div class="max-h-[90vh] overflow-y-auto rounded-2xl bg-white p-6 shadow-xl">
			<div class="flex flex-col items-center justify-center gap-4">
				<div class=" bg-white p-6">
					<div class="flex h-[500px] w-full items-center justify-center overflow-hidden rounded-xl">
						{#if !isApk}
							<picture>
								<!-- Mobile terlebih dahulu -->
								<source srcset={srcMobileMode} media="(max-width: 640px)" />
								<!-- Fallback desktop -->
								<img {src} alt={title} class="h-full w-full object-cover" />
							</picture>
						{:else}
							<img {src} alt={title} class="h-full w-full object-cover" />
						{/if}
					</div>
				</div>

				<h1 class="text-3xl font-semibold">{title}</h1>

				<p class="mx-auto max-w-4xl text-justify">{desc}</p>

				<div class="flex gap-4">
					<button
						class="min-w-25 rounded-3xl bg-red-500 px-6 py-2 text-white"
						on:click={() => (show = false)}>Close</button
					>
					<a href={url} target="_blank" rel="noopener noreferrer">
						{#if isApk}
							<button class="min-w-25 rounded-3xl bg-blue-500 px-6 py-2 text-white"
								>Download Aplikasi</button
							>
						{:else}
							<button class="min-w-25 rounded-3xl bg-blue-500 px-6 py-2 text-white"
								>Kunjungi Website</button
							>
						{/if}
					</a>
				</div>
			</div>
		</div>
	</div>
{/if}
