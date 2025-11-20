<script lang="ts">
	import Icon from 'svelte-awesome/components/Icon.svelte';
	import {
		faUser,
		faCoffee,
		faCircleUser,
		faAngleLeft,
		faChevronRight,
		faAngleRight
	} from '@fortawesome/free-solid-svg-icons';
	import { colors, ListProjectComponent } from '$lib';

	let container: HTMLElement;

	function scrollLeft() {
		container?.scrollBy({ left: -300, behavior: 'smooth' });
	}

	function scrollRight() {
		container?.scrollBy({ left: 300, behavior: 'smooth' });
	}
</script>

<div id="projects" style="background-color: {colors.darkTeal};" class="px-4 py-16 lg:px-8 xl:px-16">
	<div class="items-center justify-center gap-4">
		<div class="flex flex-col justify-center gap-4">
			<h2 class="text-center text-3xl font-semibold text-white sm:text-5xl">Project Saya</h2>
			<div class="mt-8 w-full">
				<div class="flex justify-center">
					<button class="hidden lg:block" on:click={scrollLeft}
						><Icon
							data={faAngleLeft}
							class="h-15 w-15 font-bold text-white hover:text-gray-300 xl:h-25 xl:w-25"
						/></button
					>
					<div
						bind:this={container}
						class="no-scrollbar w-full touch-pan-x overflow-x-auto scroll-smooth"
					>
						<div class="flex gap-4">
							<ListProjectComponent
								title="Website JHRIS"
								desc="JHRIS adalah aplikasi berbasis web yang dikembangkan menggunakan bahasa pemrograman PHP dengan framework CodeIgniter. Aplikasi ini digunakan oleh PT. Jadin Pratama sebagai sistem informasi kepegawaian, mencakup fitur-fitur seperti absensi, pengajuan izin, teguran, serta perhitungan denda dan tunjangan bagi karyawan."
								src="/assets/images/img_jhris.png"
								srcMobileMode="/assets/images/img_jhris_mobile_mode.png"
								url="https://jhris.jadinpratama.com"
							/>
							<ListProjectComponent
								title="JHRIS Mobile Apps"
								desc="JHRIS Mobile adalah aplikasi berbasis mobile yang dikembangkan menggunakan bahasa pemrograman Dart dengan framework Flutter, melalui platform FlutterFlow. Aplikasi ini dibuat khusus untuk karyawan PT. Jadin Pratama sebagai alat untuk melakukan absensi serta pengajuan izin atau cuti secara digital."
								src="/assets/images/img_jhris_mobile.png"
								srcMobileMode="/assets/images/img_jhris_mobile.png"
								url="/assets/apk/JHRIS_V125_new.apk"
								isApk={true}
							/>
							<ListProjectComponent
								title="Website Masuk FK"
								desc="Masuk FK adalah aplikasi website yang dikembangkan menggunakan bahasa pemrograman Typescript dengan framework Svelte. Website ini berfungsi sebagai alat untuk menguji kemampuan mahasiswa yang ingin ujian masuk fakulter kedokteran, yang dikembangkan oleh PT. Yapindo Jaya Abadi."
								src="/assets/images/img_masuk_fk.png"
								srcMobileMode="/assets/images/img_masuk_fk_mobile_mode.png"
								url="https://masuk-fk.vercel.app/"
							/>
							<ListProjectComponent
								title="BukuLoka Reader Mobile"
								desc="BukuLoka Reader adalah aplikasi mobile yang dikembangkan menggunakan bahasa pemrograman Dart dengan framework Flutter. Aplikasi ini berfungsi sebagai alat untuk membaca buku digital yang disewa melalui website BukuLoka, yang dikembangkan oleh PT. Yapindo Jaya Abadi."
								src="/assets/images/img_bukuloka_reader_mobile.png"
								srcMobileMode="/assets/images/img_jhris_mobile_mode.png"
								url="https://play.google.com/store/apps/details?id=com.yapindo.superapp.bukulokareader&pcampaignid=web_share"
								isApk={true}
							/>
							<ListProjectComponent
								title="BukuLoka Reader Desktop"
								desc="BukuLoka Reader Desktop merupakan aplikasi berbasis desktop yang dikembangkan menggunakan bahasa pemrograman Dart dengan framework Flutter. Aplikasi ini dirancang untuk memfasilitasi pengguna dalam membaca buku digital yang telah disewa melalui situs web BukuLoka. Tidak seperti versi mobile, versi desktop ini memberikan opsi akses bacaan digital melalui perangkat komputer atau laptop. Aplikasi ini merupakan bagian dari layanan digital yang disediakan oleh PT. Yapindo Jaya Abadi."
								src="/assets/images/img_bukuloka_reader_desktop.png"
								srcMobileMode="/assets/images/img_bukuloka_reader_desktop_mobile_mode.png"
								url="/assets/apk/bukuLoka_reader_v1.1.12.17.msi"
								isApk={true}
							/>
							<ListProjectComponent
								title="FITA Mobile Apps"
								desc="FITA (FIELD INTSTALLATION TECHNICAL ASISSTANCE) merupakan aplikasi berbasis mobile yang dikembangkan menggunakan bahasa pemrograman Dart dengan framework Flutter. Aplikasi ini dirancang untuk memfasilitasi teknisi dalam PT. Beyond Payment Lifecyce dalam membuat laporan pekerja manage service mesin EDC"
								src="/assets/images/img_fita_mobile.png"
								srcMobileMode="/assets/images/img_jhris_mobile_mode.png"
								url="https://github.com/albar12/ms-app-ota/releases/download/release/FITA.v2.6.21.42.apk"
								isApk={true}
							/>
							<ListProjectComponent
								title="HRIS Mobile Apps"
								desc="HRIS Mobile adalah aplikasi berbasis mobile yang dikembangkan menggunakan bahasa pemrograman Dart dengan framework Flutter. Aplikasi ini dibuat khusus untuk karyawan PT. Beyond Payment Lifecyce sebagai alat untuk melakukan absensi serta pengajuan izin atau cuti secara digital."
								src="/assets/images/img_hris_bpl.png"
								srcMobileMode="/assets/images/img_jhris_mobile_mode.png"
								url="/assets/apk/HRIS v1.0.0.apk"
								isApk={true}
							/>
						</div>
					</div>
					<button class="hidden lg:block" on:click={scrollRight}
						><Icon
							data={faAngleRight}
							class="h-15 w-15 font-bold text-white hover:text-gray-300 xl:h-25 xl:w-25"
						/></button
					>
				</div>
			</div>
		</div>
	</div>
</div>

<style>
	.no-scrollbar::-webkit-scrollbar {
		display: none;
	}
</style>
