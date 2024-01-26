<script lang="ts">
	import Footer from '$lib/Footer.svelte';
	import Header from '$lib/Header.svelte';
	import TeacherCard from '$lib/TeacherCard.svelte';
	// export let data;
</script>

<svelte:head>
	<title>ratemyprof.umt</title>
</svelte:head>

<!-- <Header isAuthenticated={data.isAuthentication} user={data.userProfile} /> -->
<!-- <Header /> -->

<main class="px-5 mt-10 flex flex-row justify-center items-center flex-wrap gap-10">
	<TeacherCard />
	<TeacherCard />
	<TeacherCard />
	<TeacherCard />
	<TeacherCard />
	<TeacherCard />
</main>
<!-- <Footer /> -->
