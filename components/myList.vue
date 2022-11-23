<script setup>
	// const { accountsData } = useAccountData()
	// import { accountService } from '@/services'
	const runtimeConfig = useRuntimeConfig()
	/* 	let accounts = ref('')
	const error = ref('')
	const pending = ref('')
 */
	/* 	accountService.getAll().then(
		(data) => {
			accounts.value = data
		},
		(error) => {
			error.value = error
		}
	) */
	const {
		data: accounts,
		pending,
		error,
		refresh,
	} = await useFetch('/accounts/getall', {
		initialCache: false,
		method: 'get',
		headers: {
			firebaseapikey: runtimeConfig.apiSecret,
		},
	})

	const deleteFromDB = async (itemId) => {
		const { pending, error, refresh } = await useFetch(`/accounts/${itemId}`, {
			method: 'delete',
			headers: {
				firebaseapikey: runtimeConfig.apiSecret,
			},
		})
	}
	const checkId = (item, itemId) => {
		// console.log('in checkId id = ', item.account_id !== itemId)
		return item.account_id !== itemId
	}
	const deleteFromBrowser = (itemId) => {
		console.log('mylist deleteFromBrowser itemId= ', itemId)
		console.log('mylist deleteFromBrowser accounts= ', accounts.value)
		accounts.value = accounts.value.filter((item) => checkId(item, itemId))

		// console.log('mylist deleteFromBrowser accounts after = ', accounts)
	}

	const deleteItem = (id) => {
		const itemId = parseInt(id)
		deleteFromDB(itemId)
		deleteFromBrowser(itemId)
	}
</script>

<template>
	<div class="root">
		<p>pending= {{ pending }}</p>
		<p>error= {{ error }}</p>
		<div v-if="pending">Loading ...</div>
		<div v-if="error">Error ...</div>
		<!-- <p>accountData {{ accountData }}</p> -->
		<div v-for="item in accounts">
			<h3>{{ item.member_firstname }} {{ item.member_lastname }}</h3>
			<p>{{ item.account_email }}</p>
			<p>{{ item.dt }}</p>
			<p>
				<nuxt-link
					class="btn btn-outline-primary"
					:to="`/admin/accounts/${item.account_id}`"
					>Edit</nuxt-link
				>
				<button
					type="button"
					class="btn btn-outline-danger"
					@click="deleteItem(item.account_id)"
				>
					Delete
				</button>
			</p>
		</div>
	</div>
</template>

<style scoped></style>
