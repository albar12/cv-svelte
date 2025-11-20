<script lang="ts">
	import { colors, TechStackComponent } from '$lib';
</script>

<div id="home" style="background-color: {colors.darkTeal};" class="px-4 py-16 lg:px-8 xl:px-16">
	<div class="flex flex-col-reverse items-center justify-center p-6 sm:mt-0 lg:flex-row">
		<div class="max-w-2xl">
			<div class="mt-8 flex flex-col items-center lg:items-start">
				<h2
					class=" text-center text-3xl font-semibold tracking-tight text-balance text-white sm:text-5xl lg:text-left"
				>
					Hello!
				</h2>
				<h1
					class="text-center text-3xl font-semibold tracking-tight text-balance text-white sm:text-5xl lg:text-left"
				>
					Saya, Alif Akbar
				</h1>
				<h3
					style="color: {colors.lightBeige};"
					class="mt-4 text-center text-2xl font-semibold tracking-tight text-balance lg:text-left"
				>
					Web Developer & Programmer
				</h3>
				<p
					class="mt-8 text-center text-justify text-lg font-medium text-pretty text-white sm:text-xl/8 lg:text-left"
				>
					Saya berpengalaman sebagai IT Programmer yang berkualitas dan profesional, Menyelesaikan
					pendidikan sarjana jurusan Teknik Informatika. Merupakan individu yang jujur, disiplin,
					komunikatif dan bertanggung jawab.
				</p>
				<a
					href="/assets/doc/cv_alif_akbar_latest.pdf"
					class="mt-4 w-[150px] rounded-2xl border border-white py-2 text-center text-white hover:bg-white hover:text-black"
					target="_blank"
					rel="noopener noreferrer"
				>
					Download CV</a
				>
			</div>
		</div>
		<div class="h-80 w-full max-w-xs sm:h-100 sm:max-w-sm md:h-150 md:max-w-md lg:max-w-lg">
			<img src="/assets/images/img_alif.png" alt="img" class="h-full w-full object-cover" />
		</div>
	</div>
</div>
<div style="background-color: {colors.deepTealGreen};" class="px-6 py-12 lg:px-8 xl:px-16">
	<div class="items-center justify-center gap-4">
		<h3
			class="text-center text-3xl font-semibold tracking-tight text-balance text-white sm:text-3xl"
		>
			TECH STACK:
		</h3>
		<div class="mt-8 w-full">
			<div class="no-scrollbar w-full touch-pan-x overflow-x-auto scroll-smooth">
				<div class="flex gap-4 xl:items-center xl:justify-center">
					<TechStackComponent src="/assets/icons/ic_html.svg" title="HTML" />
					<TechStackComponent src="/assets/icons/ic_php.svg" title="PHP" />
					<TechStackComponent src="/assets/icons/ic_jquery.svg" title="Jquery" />
					<TechStackComponent src="/assets/icons/ic_bootstrap.svg" title="Bootstrap" />
					<TechStackComponent src="/assets/icons/ic_tailwind.svg" title="Tailwind" />
					<TechStackComponent src="/assets/icons/ic_javascript.svg" title="Javascript" />
					<TechStackComponent src="/assets/icons/ic_typescript.svg" title="Typescript" />
					<TechStackComponent src="/assets/icons/ic_express.svg" title="Express" />
					<TechStackComponent src="/assets/icons/ic_svelte.svg" title="Svelte" />
					<TechStackComponent src="/assets/icons/ic_flutter.svg" title="Flutter" />
				</div>
			</div>
		</div>
	</div>
</div>
