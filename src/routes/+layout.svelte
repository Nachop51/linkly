<script lang="ts">
	import '../app.css'
	import { page } from '$app/stores'
	import NavBar from '$lib/components/NavBar.svelte'

	$: user = $page.data.session?.user
</script>

<svelte:head>
	<title>Linkly</title>
	<meta name="description" content="Short your links with Linkly in just one go." />
</svelte:head>

<NavBar {user} />

<div class="min-h-size mt-24 relative">
	<slot />
</div>
