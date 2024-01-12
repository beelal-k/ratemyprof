<script lang="ts">
	import '../app.css';
	import Header from '../components/Header.svelte';
</script>

<section>
	<Header />
	<slot />
</section>

<style>
	section {
        padding-top: 2em;
        padding-inline: 5em;
	}
</style>
