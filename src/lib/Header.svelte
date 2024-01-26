<script lang="ts">
	import type {UserType} from '@kinde-oss/kinde-auth-sveltekit';

	export let user: UserType | null;
	export let isAuthenticated: boolean;
</script>

<main class="flex flex-row justify-between align-center">
	<a href="/">
		<h1 class="text-3xl font-semibold w-1/3 flex items-center">
			rateMyProf<span class="text-[#E10000]">.umt</span>
		</h1>
	</a>
	<div class="w-2/5">
		<input
			type="text"
			placeholder="Search"
			class="border border-lightgray-100 px-5 py-2 text-xl rounded w-full outline-none"
		/>
	</div>
	<div class="w-auto flex flex-row justify-end items-center gap-5">
		{#if isAuthenticated}
			<p class="text-xl">Hello, {user?.given_name} {user?.family_name}</p>
			<p />
			<a
				href="api/auth/logout"
				class="border border-[#1a1a1a] font-semibold px-5 py-1 rounded text-lg">Logout</a
			>
			{#if user?.email === 's2023065086@umt.edu.pk'}
				<a href="/admin-panel">
					<p>Admin panel</p>
				</a>
			{/if}
		{:else}
			<a
				href="api/auth/login"
				class="border border-[#1a1a1a] font-semibold px-5 py-1 rounded text-lg">Login</a
			>
			<a
				href="/api/auth/register"
				class="border border-[#e10000] bg-[#E10000] text-white font-semibold px-4 py-1 rounded text-lg"
				>Signup</a
			>
		{/if}
	</div>
</main>

<!-- <script lang="ts">
	import type {UserType} from '@kinde-oss/kinde-auth-sveltekit';

	export let user: UserType | null;
	export let isAuthenticated: boolean;
</script>

<header>
	<nav class="nav container">
		<h1 class="text-display-3">KindeAuth</h1>
		{#if isAuthenticated}
			<div class="profile-blob">
				<div class="avatar">
					{user?.given_name}
				</div>
				<div>
					<p class="text-heading-2 text-capitalize">
						{user?.given_name}
						{user?.family_name}
					</p>
					<a class="text-subtle" href="/api/auth/logout"> Sign out </a>
				</div>
			</div>
		{:else}
			<div>
				<a class="btn btn-ghost sign-in-btn" href="/api/auth/login"> Sign in </a>
				<a class="btn btn-dark" href="/api/auth/register"> Sign up </a>
			</div>
		{/if}
	</nav>
</header> -->

<style></style>
