<script lang="ts">
	import {getContext} from 'svelte';
	import type {currentUser} from '$lib/types/custom';

	let user: currentUser = getContext('user');
</script>

<main>
	{#if user?.user.email === 's2023065086@umt.edu.pk'}
		<h1>Admin Panel</h1>
	{:else}
		<h1>Whoops! You're not supposed to be here</h1>
	{/if}
</main>

<style></style>
