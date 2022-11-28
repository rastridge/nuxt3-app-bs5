<template>
	<header>
		<nav
			class="navbar navbar-expand-md navbar-dark bg-success p-3 fixed-top shadow"
		>
			<div class="container">
				<button
					class="navbar-toggler"
					type="button"
					data-bs-toggle="collapse"
					data-bs-target="#navbarSupportedContent"
					aria-controls="navbarSupportedContent"
					aria-expanded="false"
					aria-label="Toggle navigation"
				>
					<span class="navbar-toggler-icon"></span>
				</button>
				<nuxt-link class="navbar-brand" to="/"
					>Nuxt 3 with Bootstrap5 and Primevue</nuxt-link
				>

				<div class="collapse navbar-collapse" id="navbarSupportedContent">
					<ul class="navbar-nav mx-auto mb-2 mb-lg-0">
						<li class="nav-item">
							<nuxt-link class="nav-link" to="/">Home</nuxt-link>
						</li>
						<li class="nav-item">
							<nuxt-link class="nav-link" to="/editor">Editor</nuxt-link>
						</li>
						<li class="nav-item">
							<nuxt-link class="nav-link" to="/autocomplete"
								>Autocomplete</nuxt-link
							>
						</li>
						<li class="nav-item">
							<nuxt-link class="nav-link" to="/datepicker"
								>Date Picker</nuxt-link
							>
						</li>
						<li class="nav-item">
							<nuxt-link class="nav-link" to="/admin/accounts">List</nuxt-link>
						</li>
						<li class="nav-item dropdown">
							<a
								class="nav-link dropdown-toggle"
								href="#"
								role="button"
								data-bs-toggle="dropdown"
								aria-expanded="false"
							>
								Dropdown
							</a>
							<ul class="dropdown-menu">
								<li><a class="dropdown-item" href="#">Action</a></li>
								<li>
									<a class="dropdown-item" href="#">Another action</a>
								</li>
								<li><hr class="dropdown-divider" /></li>
								<li>
									<a class="dropdown-item" href="#">Something else here</a>
								</li>
							</ul>
						</li>
					</ul>
				</div>
			</div>
		</nav>
		>
	</header>
</template>

<style scoped></style>
