<script lang="ts">
	import '../app.css';
	import Header from '$lib/Header.svelte';
	import {setContext} from 'svelte';

	export let data;

	const userContext = {
		auth: data.isAuthentication,
		user: data.userProfile
	};

	setContext('user', userContext);
</script>

<section>
	<Header isAuthenticated={data.isAuthentication} user={data.userProfile} />
	<slot />
</section>

<style>
	section {
		padding-top: 2em;
		padding-inline: 5em;
	}
</style>
