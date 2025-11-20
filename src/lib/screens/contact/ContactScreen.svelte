<script lang="ts">
	import emailjs from '@emailjs/browser';
	import { toast } from '@zerodevx/svelte-toast';
	import { colors, TechStackComponent } from '$lib';

	let show = false;
	let namaLengkap = '';
	let subject = '';
	let email = '';
	let message = '';

	let loading = false;
	let success = '';
	let errorMsg = '';

	async function sendEmail() {
		loading = true;
		try {
			const response = await emailjs.send(
				'service_gltudfc',
				'template_2l1sfll',
				{
					from_name: namaLengkap,
					subject: subject,
					from_email: email,
					message: message
				},
				'uqo4AufmpVpuTbwtp'
			);
			successToast('Your message has been sent!');
			loading = false;
			namaLengkap = '';
			email = '';
			message = '';
		} catch (error) {
			loading = false;
			errorToast('Failed to send message.');
		}
	}

	function successToast(msg: string) {
		toast.push(msg, {
			theme: {
				'--toastBackground': colors.freshGreen,
				'--toastColor': 'white',
				'--toastBorderRadius': '10px'
			},
			classes: ['rounded-2xl', 'p-4']
		});
	}

	function errorToast(msg: string) {
		toast.push(msg, {
			theme: {
				'--toastBackground': 'red',
				'--toastColor': 'white'
			}
		});
	}
</script>

<div id="contact" style="background-color: {colors.darkTeal};" class="px-4 py-16 lg:px-8 xl:px-32">
	<h1 class="text-center text-3xl font-semibold tracking-tight text-balance text-white md:text-5xl">
		Kontak Saya
	</h1>
	<div class="mt-4 flex flex-col items-center justify-center p-6 lg:flex-row">
		<div class="flex w-full flex-col gap-4 rounded-2xl border border-white p-6 lg:flex-row">
			<div class="flex w-full flex-col gap-4 rounded-2xl bg-white p-6 lg:max-w-xl">
				<div class="text-center text-2xl font-bold text-black lg:text-left">GET IN TOUCH</div>
				<div class="text-justify text-gray-500 lg:text-left">
					if you have any question. Please feel free to get in touch with me. Send me a message and
					i'll respond as soon as possible.
				</div>
				<div class="flex flex-col gap-1">
					<label class="font-semibold text-black" for="nama-lengkap">Name</label>
					<input
						bind:value={namaLengkap}
						type="text"
						id="nama-lengkap"
						placeholder="Nama Lengkap"
						class="rounded-xl border border-black p-2"
					/>
				</div>
				<div class="flex flex-col gap-1">
					<label class="font-semibold text-black" for="subject">Subject</label>
					<input
						bind:value={subject}
						type="text"
						id="subject"
						placeholder="Subject"
						class="rounded-xl border border-black p-2"
					/>
				</div>
				<div class="flex flex-col gap-1">
					<label class="font-semibold text-black" for="email">Email</label>
					<input
						bind:value={email}
						type="text"
						id="email"
						placeholder="Email"
						class="rounded-xl border border-black p-2"
					/>
				</div>
				<div class="flex flex-col gap-1">
					<label class="font-semibold text-black" for="message">Message</label>
					<textarea
						bind:value={message}
						id="message"
						placeholder="Message"
						class="rounded-xl border border-black p-2"
					></textarea>
				</div>

				<button
					class="flex justify-center rounded-2xl bg-green-500 p-2 text-white hover:bg-green-600"
					on:click={() => sendEmail()}
				>
					{#if loading}
						<div
							class="h-7 w-7 animate-spin rounded-full border-4 border-white border-t-transparent"
						></div>
					{:else}
						Send Message
					{/if}
				</button>
			</div>
			<div class="w-full rounded-2xl">
				<iframe
					title="Lokasi Saya"
					src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3966.3407211555045!2d106.67087547586803!3d-6.218721460910274!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2e69f97f1d95d9c7%3A0x5111f5830a9db58b!2sJl.%20Rajawali%20Blok%20K2%20No.3%2C%20Kunciran%20Indah%2C%20Kec.%20Pinang%2C%20Kota%20Tangerang%2C%20Banten%2015144!5e0!3m2!1sen!2sid!4v1763546648375!5m2!1sen!2sid"
					class="h-150 w-full rounded-2xl"
					style="border:0;"
					allowfullscreen={true}
					loading="lazy"
					referrerpolicy="no-referrer-when-downgrade"
				></iframe>
			</div>
		</div>
	</div>
</div>
