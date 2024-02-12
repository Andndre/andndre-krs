<script lang="ts">

	import Container from "$lib/components/my/Container.svelte";
	import * as Carousel from "$lib/components/ui/carousel";
	import * as Card from "$lib/components/ui/card";
	import projects from '$lib/projects.json'
	import { Badge } from "$lib/components/ui/badge";
	import Button from "$lib/components/ui/button/button.svelte";
	import type { CarouselAPI } from "$lib/components/ui/carousel/context.js";
	import { toast } from "svelte-sonner";
	import { Toaster } from "$lib/components/ui/sonner";
	
  let api: CarouselAPI;
  let current = 0;
  let count = 0;
  $: if (api) {
    count = api.scrollSnapList().length;
    current = api.selectedScrollSnap() + 1;
    api.on("select", () => {
      current = api.selectedScrollSnap() + 1;
    });
  }
	
	$: if (current === count) {
		toast("Anda telah sampai di akhir project!")
	}
</script>

<Toaster />

<Container>
	<section class="w-full" id="projects">
		<h2 class="scroll-m-20 text-3xl font-bold tracking-tight transition-colors first:mt-0 text-center">
			Project
		</h2>
		<p class="text-sm text-center pt-3">Berikut ini beberapa project yang saya buat dan dipublikasikan selama proses perkuliahan</p>
		<div class="pt-8"></div>
		<Carousel.Root bind:api
		opts={{
			align: "center"
		}}
		class="w-full lg:px-12 px-4"
	>
		<Carousel.Content>
			{#each projects as project}
				<Carousel.Item class="md:basis-1/2 lg:basis-1/3">
					<div class="p-1 select-none">
						<Card.Root>
							<Card.Content class="contents"
							>
								<div class="p-6">
									<h3 class="font-bold">{project.name}</h3>
									{#if project.semester}
											<p class="text-sm text-gray-500">Semester {project.semester}</p>
											<div class="flex wrap gap-2 pt-3">
												{#each project.tags as tag}
													<Badge variant="default">{tag}</Badge>
												{/each}
											</div>
									{/if}
									<div class="flex justify-start pt-6">
										<Button href="{project.url}" variant="secondary">Lihat</Button>
									</div>
								</div>
							</Card.Content>
						</Card.Root>
					</div>
				</Carousel.Item>
			{/each}
		</Carousel.Content>
		<Carousel.Previous class="ml-8" />
		<Carousel.Next class="mr-8" />
	</Carousel.Root>
	<div class="py-2 text-center text-sm text-muted-foreground">
    Slide {current} of {count}
  </div>
</section>
</Container>
