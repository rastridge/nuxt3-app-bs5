<script setup>
	const router = useRouter()

	const onSubmit = function (state) {
		handleSubmit(state)
	}

	const handleSubmit = async function (state) {
		const runtimeConfig = useRuntimeConfig()
		await useFetch('/users/addone', {
			method: 'post',
			body: state,
			headers: {
				firebaseapikey: runtimeConfig.apiSecret,
			},
		})
		navigateTo('/admin/users')
	}
</script>

<template>
	<div>
		<Head>
			<Title>Add User</Title>
		</Head>
		<div class="text-center m-5 display-6">
			<b>Add User</b>
		</div>

		<div class="root">
			<my-user-form @submitted="onSubmit" />
		</div>
	</div>
</template>

<style scoped></style>
