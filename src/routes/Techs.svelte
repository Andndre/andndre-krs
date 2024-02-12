<script lang="ts">

	import Container from "$lib/components/my/Container.svelte";
	type Tech = {
		logo: string;
		name: string;
		description: string;
	};
	const techs: Tech[] = [
		{
			logo: '/images/astro.png',
			name: 'Astro.js',
			description:
				'Astro.js adalah platform pengembangan web modern yang memungkinkan Anda membuat situs web yang cepat, aman, dan mudah diakses.'
		},
		{
			logo: '/images/blender.png',
			name: 'Blender',
			description:
				'Blender adalah perangkat lunak sumber terbuka untuk membuat animasi, efek visual, dan model 3D.'
		},
		{
			logo: '/images/bun.png',
			name: 'Bun',
			description: 'Bun adalah...'
		},
		{
			logo: '/images/c++.png',
			name: 'C++',
			description:
				'C++ adalah bahasa pemrograman tingkat tinggi yang digunakan untuk pengembangan sistem perangkat lunak.'
		},
		{
			logo: '/images/css.svg',
			name: 'CSS',
			description:
				'CSS adalah bahasa gaya yang digunakan untuk mengatur tampilan dokumen web yang ditulis dalam HTML.'
		},
		{
			logo: '/images/deno.png',
			name: 'Deno',
			description: 'Deno adalah runtime JavaScript yang aman, cepat, dan ramah pengembang.'
		},
		{
			logo: '/images/docker.png',
			name: 'Docker',
			description:
				'Docker adalah platform perangkat lunak yang digunakan untuk membangun, menguji, dan menerapkan aplikasi dalam kontainer.'
		},
		{
			logo: '/images/drizzle.png',
			name: 'Drizzle',
			description: 'Drizzle adalah...'
		},
		{
			logo: '/images/express.png',
			name: 'Express',
			description:
				'Express adalah kerangka aplikasi web Node.js yang minimal dan fleksibel yang menyediakan seperangkat fitur kuat untuk aplikasi web dan seluler.'
		},
		{
			logo: '/images/figma.png',
			name: 'Figma',
			description:
				'Figma adalah platform desain kolaboratif berbasis web yang memungkinkan tim untuk membuat, menguji, dan menghasilkan desain bersama-sama.'
		},
		{
			logo: '/images/flutter.png',
			name: 'Flutter',
			description:
				'Flutter adalah kerangka kerja open-source yang dikembangkan oleh Google untuk membuat aplikasi mobile, web, dan desktop dari satu kode basis.'
		},
		{
			logo: '/images/git.png',
			name: 'Git',
			description:
				'Git adalah sistem kontrol versi yang digunakan untuk melacak perubahan dalam kode sumber selama pengembangan perangkat lunak.'
		},
		{
			logo: '/images/github.png',
			name: 'GitHub',
			description:
				'GitHub adalah platform pengembangan perangkat lunak berbasis web yang menggunakan Git untuk kontrol versi dan kolaborasi.'
		},
		{
			logo: '/images/hf-logo.png',
			name: 'Hugging Face',
			description:
				'Hugging Face adalah perusahaan yang mengembangkan dan memelihara model bahasa alami berkinerja tinggi.'
		},
		{
			logo: '/images/html.webp',
			name: 'HTML',
			description:
				'HTML adalah bahasa markup standar untuk dokumen yang dirancang untuk ditampilkan di peramban web.'
		},
		{
			logo: '/images/java.png',
			name: 'Java',
			description:
				'Java adalah bahasa pemrograman yang digunakan untuk mengembangkan aplikasi perangkat lunak dan layanan.'
		},
		{
			logo: '/images/javascript.png',
			name: 'JavaScript',
			description:
				'JavaScript adalah bahasa pemrograman tingkat tinggi yang digunakan untuk membuat dan mengelola konten interaktif di situs web.'
		},
		{
			logo: '/images/laragon.png',
			name: 'Laragon',
			description:
				'Laragon adalah lingkungan pengembangan PHP yang ringan, cepat, dan kuat untuk Windows.'
		},
		{
			logo: '/images/laravel.png',
			name: 'Laravel',
			description:
				'Laravel adalah kerangka kerja aplikasi web dengan sintaks yang elegan dan ekspresif.'
		},
		{
			logo: '/images/mongodb.png',
			name: 'MongoDB',
			description: 'MongoDB adalah basis data NoSQL yang menggunakan dokumen untuk menyimpan data.'
		},
		{
			logo: '/images/mysql.png',
			name: 'MySQL',
			description:
				'MySQL adalah sistem manajemen basis data relasional open-source yang menggunakan bahasa SQL.'
		},
		{
			logo: '/images/next.png',
			name: 'Next.js',
			description:
				'Next.js adalah kerangka kerja aplikasi web React yang memungkinkan Anda membuat aplikasi web dengan cepat.'
		},
		{
			logo: '/images/php.png',
			name: 'PHP',
			description: 'PHP adalah bahasa skrip sisi server yang digunakan untuk pengembangan web.'
		},
		{
			logo: '/images/postman.png',
			name: 'Postman',
			description: 'Postman adalah platform kolaborasi untuk pengembang API.'
		},
		{
			logo: '/images/python.png',
			name: 'Python',
			description:
				'Python adalah bahasa pemrograman tingkat tinggi yang digunakan untuk pengembangan web, analisis data, dan kecerdasan buatan.'
		},
		{
			logo: '/images/react.png',
			name: 'React',
			description: 'React adalah pustaka JavaScript untuk membangun antarmuka pengguna.'
		},
		{
			logo: '/images/redis.png',
			name: 'Redis',
			description:
				'Redis adalah basis data open-source yang menggunakan struktur data di dalam memori.'
		},
		{
			logo: '/images/socket-io.png',
			name: 'Socket.IO',
			description: 'Socket.IO adalah pustaka JavaScript untuk aplikasi web real-time.'
		},
		{
			logo: '/images/svelte.png',
			name: 'Svelte',
			description:
				'Svelte adalah kerangka kerja JavaScript yang memungkinkan Anda menulis kode yang lebih efisien.'
		},
		{
			logo: '/images/swagger.png',
			name: 'Swagger',
			description: 'Swagger adalah alat untuk merancang, membangun, dan mendokumentasikan API.'
		},
		{
			logo: '/images/tailwind.png',
			name: 'Tailwind CSS',
			description:
				'Tailwind CSS adalah kerangka kerja CSS yang memungkinkan Anda membuat desain web yang responsif dan menarik.'
		},
		{
			logo: '/images/typescript.webp',
			name: 'TypeScript',
			description:
				'TypeScript adalah bahasa pemrograman open-source yang merupakan superset dari JavaScript.'
		},
		{
			logo: '/images/vscode.png',
			name: 'Visual Studio Code',
			description: 'Visual Studio Code adalah editor kode sumber yang dikembangkan oleh Microsoft.'
		},
		{
			logo: '/images/wordpress.png',
			name: 'WordPress',
			description:
				'WordPress adalah sistem manajemen konten open-source yang digunakan untuk membuat situs web dan blog.'
		}
	];

</script>
<section id="techs" class="py-20">
	<Container>
		<h2
			class="scroll-m-20 text-3xl font-bold tracking-tight transition-colors first:mt-0 text-center"
		>
			Tech
		</h2>
		<p class="text-sm text-center pt-3">
			Di waktu luang saya, saya telah mempelajari beberapa teknologi berikut.
		</p>
		<div class="mt-8"></div>
		<div class="flex justify-center flex-wrap gap-4">
			{#each techs as tech}
				<img
					src={tech.logo}
					alt={tech.name}
					title={tech.description}
					class="filter grayscale hover:filter-none transition-all duration-300 h-6"
				/>
			{/each}
		</div>
	</Container>
</section>
