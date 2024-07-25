<script lang="ts">
	import type { AnimeProp } from '$lib';

	let { id, name, image, kind, episodes, score, episodes_aired }: AnimeProp = $props();
</script>

<div class="max-w-sm rounded relative w-full">
	<div class="relative w-full h-[37vh]">
		<img
			src={`https://shikimori.one${image.original}`}
			alt={name}
			class="object-fill w-full h-full rounded-md"
		/>
	</div>

	<div class="py-4 flex flex-col gap-3">
		<!-- NAME -->
		<div class="flex justify-between items-center gap-1">
			<h2 class="font-bold text-white text-xl line-clamp-1 w-full">
				{name}
			</h2>

			<!-- KIND -->
			<div class="py-1 px-2 bg-[#161921] rounded-sm">
				<p class="text-white text-sm font-bold capitalize">
					{kind}
				</p>
			</div>
		</div>

		<div class="flex gap-4 items-center">
			<!-- EPISODES -->
			<div class="flex flex-row gap-2 items-center">
				<img src="/assets/svg/episodes.svg" alt="episodes" class="object-contain" />
				<p class="text-base text-white font-bold">
					{episodes || episodes_aired}
				</p>
			</div>

			<!-- SCORE -->
			<div class="flex flex-row gap-2 items-center">
				<img src="/assets/svg/star.svg" alt="star" class="object-contain" />
				<p class="text-base font-bold text-[#FFAD49]">{score}</p>
			</div>
		</div>
	</div>
</div>
