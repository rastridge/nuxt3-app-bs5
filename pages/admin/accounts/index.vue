<template>
	<div>
		<Head>
			<Title>Accounts List</Title>
		</Head>

		<div class="root">
			<b>Account List</b>
		</div>
		<div class="root">
			<nuxt-link class="nav-link" to="/admin/accounts/add">Add</nuxt-link>
		</div>

		<div>
			<my-list />
		</div>
	</div>
</template>
<script setup>
	clearNuxtData()
</script>
