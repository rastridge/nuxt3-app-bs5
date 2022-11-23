<template>
	<div class="container py-4">
		<div class="row">
			<div class="h-100 p-5 text-white bg-dark rounded-2">
				<p>error.statusMessage= {{ error.statusMessage }}</p>
				<p>error.statusCode= {{ error.statusCode }}</p>
				<button class="btn btn-primary btn-lg" @click="handleError">
					Clear errors
				</button>
			</div>
		</div>
	</div>
</template>

<script setup>
	// const props = defineProps({
	// 	error: Object,
	// })
	defineProps(['error'])
	const handleError = () => clearError({ redirect: '/' })
</script>
