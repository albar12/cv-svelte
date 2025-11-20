<script lang="ts">
	import { colors, ContactListComponent, SosialMediaComponent } from '$lib';
	import {
		faGithub,
		faInstagram,
		faLinkedin,
		faWhatsapp
	} from '@fortawesome/free-brands-svg-icons';
	import { faEnvelope, faLocationDot } from '@fortawesome/free-solid-svg-icons';
</script>

<div id="about" style="background-color: {colors.darkTeal};" class="px-4 lg:px-8 lg:py-16 xl:px-16">
	<div class="lg:items-top flex flex-col items-center justify-center lg:flex-row">
		<div class="h-80 w-full max-w-xs sm:h-100 sm:max-w-sm md:h-150 md:max-w-md lg:max-w-lg">
			<img
				src="/assets/images/img_alif_secondary.png"
				alt="img"
				class="h-full w-full object-cover"
			/>
		</div>
		<div class="max-w-2xl">
			<div class="mt-8 flex flex-col items-center lg:items-start">
				<h1
					class="text-center text-3xl font-semibold tracking-tight text-balance text-white sm:text-5xl lg:text-left"
				>
					Tentang Saya
				</h1>
				<p
					class="mt-8 text-center text-justify text-lg font-medium text-pretty text-white md:text-xl lg:text-left"
				>
					Halo, saya Alif Akbar, lahir di Jakarta pada 08 Agustus 1998. Saya adalah seorang IT
					Programmer dengan pengalaman dalam pengembangan aplikasi serta pemecahan masalah teknis
					secara efektif dan profesional. Saya menyelesaikan pendidikan sarjana di Teknik
					Informatika, yang menjadi dasar kuat bagi kemampuan teknis dan analitis saya. Dalam
					bekerja, saya selalu menjunjung tinggi nilai kejujuran, disiplin, serta mampu
					berkomunikasi dengan baik dalam tim maupun individu. Saya juga memiliki rasa tanggung
					jawab yang tinggi dan selalu berusaha memberikan hasil terbaik pada setiap proyek yang
					saya tangani.
				</p>
			</div>
			<div class="flex flex-col items-start">
				<ContactListComponent data={faEnvelope} title="Email" desc="akbaralif74@gmail.com" />
				<ContactListComponent data={faLocationDot} title="Location" desc="Tangerang, Indonesia" />
				<ContactListComponent data={faWhatsapp} title="Phone" desc="+62 812-1404-4836" />
			</div>
			<div class="mt-8">
				<h3 class="text-left text-xl font-semibold tracking-tight text-balance text-white">
					FIND ME ON :
				</h3>
				<div class="mt-4 flex flex-col gap-4 lg:flex-row">
					<SosialMediaComponent
						data={faLinkedin}
						url="https://www.linkedin.com/in/alif-akbar-66b202160"
					/>
					<SosialMediaComponent data={faInstagram} url="https://www.instagram.com/akbaralif74/" />
					<SosialMediaComponent data={faGithub} url="https://github.com/albar12" />
				</div>
			</div>
		</div>
	</div>
</div>
