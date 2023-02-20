<script>
	import { fly } from 'svelte/transition';
	import { sineInOut } from 'svelte/easing';
	export let pathname = "";
</script>

{#key pathname}
	<!--
	<div in:fly={{ x: 5, duration: 1500, delay: 1500 }}
		 out:fly={{ x: -5, duration: 1500 }}
	>-->
	<div in:fly={{ opacity: 0, duration: 2000, delay: 2000, easing: sineInOut }}
		 out:fly={{ opacity: 0, duration: 2000 }}
	>
		<slot />
	</div>
{/key}