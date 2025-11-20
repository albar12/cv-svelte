<script lang="ts">
	export let title: string;
	export let src: string;
</script>

<tooltip text={title}>
	<div
		class="flex h-[50px] w-[50px] items-center justify-center rounded-2xl bg-white p-2 md:h-[100px] md:w-[100px] md:p-4"
	>
		<img {src} alt="icon" {title} />
	</div>
</tooltip>
