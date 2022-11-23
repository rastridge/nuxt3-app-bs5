<template>
	<div class="container">
		<div class="d-flex w-100 h-100 p-3 text-center mx-auto flex-column">
			<p>X: {{ x }} Y: {{ y }}</p>
			<p>route = {{ route.path }}</p>
			<p>route params = {{ route.params.id }}</p>
			<my-header />
			<!-- <div>
				<h6>Color mode: {{ $colorMode.value }}</h6>
				<select v-model="$colorMode.preference">
					<option value="system">System</option>
					<option value="light">Light</option>
					<option value="dark">Dark</option>
					<option value="sepia">Sepia</option>
				</select>
			</div> -->

			<slot />
			<my-footer />
		</div>
	</div>
</template>

<script setup>
	import { useMouse } from '@/composables/useMouse'
	import '@formkit/themes/genesis'
	// const colorMode = useColorMode()
	const { x, y } = useMouse()
	const route = useRoute()
</script>

<style>
	/* body {
		background-color: #fff;
		color: rgba(0, 0, 0, 0.8);
		text-shadow: 0 0.05rem 0.1rem rgba(0, 0, 0, 0.5);
		box-shadow: inset 0 0 5rem rgba(0, 0, 0, 0.5);
	}
	.dark-mode body {
		background-color: #091a28;
		color: #ebf4f1;
	}
	.sepia-mode body {
		background-color: #f1e7d0;
		color: #433422;
	}

	 */
	body {
		background-color: rgb(183, 134, 134);
	}
	.root {
		max-width: 600px;
		margin: 0 auto;
		padding: 2rem;
		margin-top: 3rem;
		border: solid thick green;
		border-radius: 20px;
		background-color: rgba(245, 245, 245, 0.528);
	}

	.bd-placeholder-img {
		font-size: 1.125rem;
		text-anchor: middle;
		-webkit-user-select: none;
		-moz-user-select: none;
		user-select: none;
	}

	@media (min-width: 768px) {
		.bd-placeholder-img-lg {
			font-size: 3.5rem;
		}
	}
</style>
