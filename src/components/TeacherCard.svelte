<script>
	import professor from '$lib/assets/professor.jpg';
	import starFilled from '$lib/assets/starFilled.png';
	import starOutline from '$lib/assets/starOutline.png';
</script>

<main class="flex flex-col border w-1/5 rounded p-3">
	<img src={professor} alt="Professor" class="rounded" />
	<p class="text-xl py-2">Dr Ehtesham Ul Haq Dar</p>
	<div class="flex flex-row justify-start items-center">
		<img src={starFilled} alt="Professor" class="rounded" />
		<img src={starFilled} alt="Professor" class="rounded" />
		<img src={starFilled} alt="Professor" class="rounded" />
		<img src={starOutline} alt="Professor" class="rounded" />
		<img src={starOutline} alt="Professor" class="rounded" />
		<p id="reviews" class="ml-2">(12)</p>
	</div>
	<p class="py-2 text-lg">Dept: BSSE, BSCS</p>
</main>

<style></style>
