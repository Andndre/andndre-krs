<script lang="ts">

	import Container from "$lib/components/my/Container.svelte";
	import LucideIcon from "$lib/components/my/LucideIcon.svelte";
	import Button from "$lib/components/ui/button/button.svelte";
	import Separator from "$lib/components/ui/separator/separator.svelte";
	type Contact = {
		name: string;
		url: string;
		icon: string;
	};

	const contacts: Contact[] = [
		{
			name: 'Github',
			url: 'https://github.com/Andndre',
			icon: 'Github'
		},
		{
			name: 'Instagram',
			url: 'https://instagram/g.ndre',
			icon: 'Instagram'
		},
		{
			name: 'Email',
			url: 'mailto:agungandre687@gmail.com',
			icon: 'Mail'
		}
	];
</script>

<div class="relative" id="home">
	<div
		aria-hidden="true"
		class="absolute inset-0 grid grid-cols-2 -space-x-52 opacity-40 dark:opacity-20"
	>
		<div
			class="blur-[106px] h-56 bg-gradient-to-br from-green-200 to-blue-400 dark:from-gray-700"
		></div>
		<div
			class="blur-[106px] h-32 bg-gradient-to-r from-cyan-400 to-sky-300 dark:to-green-600"
		></div>
	</div>
	<Container>
		<div class="relative pt-36 ml-auto">
			<div class="lg:w-5/6 flex mx-auto items-end">
				<div class="text-left flex-[3]">
					<h1 class="scroll-m-20 text-4xl font-extrabold tracking-tight lg:text-5xl">
						Hello, world! <br />Nama saya <span class="text-blue-500 dark:text-white">Andre.</span>
					</h1>
					<p class="mt-8 text-gray-700 dark:text-gray-300 text-sm">
						Saya mahasiswa Undiksha jurusan Teknik Informatika
					</p>
					<div class="mt-8 mb-8 flex flex-wrap justify-start gap-y-4 gap-x-3">
						<Button href="mailto:agungandre687@gmail.com">Hubungi Saya</Button>
						<Button href="#about-me" variant="secondary">Tentang Saya</Button>
					</div>
					<div class="flex gap-3">
						{#each contacts as contact, i}
							{#if i != 0}
								<Separator orientation="vertical" />
							{/if}
							<a
								href={contact.url}
								title={contact.name}
								class="p-3 rounded-full bg-secondary hover:bg-blue-400"
							>
								<LucideIcon name={contact.icon} />
							</a>
						{/each}
					</div>
				</div>
				<div class="hidden lg:block flex-[2] border-b-2 border-b-blue-400">
					<img src="/images/andre.png" alt="hero" />
				</div>
			</div>
		</div>
	</Container>
</div>
