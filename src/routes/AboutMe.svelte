<script lang="ts">

	import Container from "$lib/components/my/Container.svelte";
	import { Highlight, LineNumbers } from "svelte-highlight";
	import { typescript } from "svelte-highlight/languages/typescript";


	const contentAboutMe = `Nama saya Anak Agung Gede Andre Kusuma, berasal dari Desa Timuhun, Klungkung, Bali. Saat
ini, saya sedang menempuh pendidikan di Jurusan Teknik Informatika, Universitas Pendidikan
Ganesha Bali. Selama perjalanan pendidikan saya, saya telah aktif terlibat dalam beberapa
proyek pemrograman di luar lingkup perkuliahan. Beberapa di antaranya mencakup
pengembangan website, API, dan proyek pemrograman lainnya. Keahlian utama saya terletak di
bidang Frontend, di mana saya memiliki pengalaman dengan beberapa framework seperti HTML +
CSS, React, Svelte, dan Laravel. Selain itu, saya juga memiliki pemahaman mendalam tentang
konsep pemrograman Backend, termasuk penguasaan konsep-konsep seperti API, komunikasi
real-time dengan Web Socket, dan Web RTC di berbagai framework. Bahasa pemrograman utama
saya adalah Typescript (Javascript). Selain itu, saya juga memiliki pengetahuan dalam
bahasa pemrograman lain seperti Python, C++, C#, Dart (Flutter), Java, dan Golang. Saya
selalu bersemangat untuk terus mengembangkan keterampilan dan pengetahuan saya di dunia
pemrograman, serta siap untuk menghadapi tantangan baru yang muncul dalam industri
teknologi`

const aboutMe = `const aboutMe = \`
${contentAboutMe}
\`
console.log(aboutMe);`
</script>
<section class="mt-16" id="about-me">
	<Container class="lg:w-5/6 mx-auto bg-blue-100/50 border border-gray-400 flex p-4 lg:p-6 flex-col lg:flex-row gap-3 rounded-xl shadow-sm">
		<div class="space-y-3 mx-auto pt-3">
			<h2 class="scroll-m-20 text-3xl lg:text-center font-bold tracking-tight transition-colors first:mt-0">
				Tentang saya
			</h2>
			<div class="pt-4"></div>
			<p class="lg:hidden text-justify">
				{contentAboutMe}
			</p>
			<div class="hidden lg:block code-wrapper">
				<Highlight class="rounded-md lg:mx-auto" language={typescript} code={aboutMe} let:highlighted>
					<LineNumbers {highlighted} startingLineNumber={42} />
				</Highlight>
			</div>
		</div>
	</Container>
</section>
