<template>
	<div>
		<b-jumbotron
			bg-variant="info"
			text-variant="white"
			border-variant="dark"
			fluid
			header="Error"
		>
			<p>error.statusMessage= {{ error.statusMessage }}</p>
			<p>error.statusCode= {{ error.statusCode }}</p>
			<b-button variant="primary" @click="handleError">Clear errors</b-button>
		</b-jumbotron>
	</div>
</template>

<script setup>
	// const props = defineProps({
	// 	error: Object,
	// })
	defineProps(['error'])
	const handleError = () => clearError({ redirect: '/' })
</script>
