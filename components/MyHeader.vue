<template>
	<header class="mb-auto">
		<div>
			<nav
				class="navbar navbar-expand-md bg-primary navbar-dark justify-content-center"
			>
				<!-- Brand -->
				<a class="navbar-brand" href="#">Nuxt 3+Bootstrap5+Bootswatch</a>

				<!-- Links -->
				<ul class="navbar-nav">
					<li class="nav-item">
						<nuxt-link class="nav-link" to="/">Home</nuxt-link>
					</li>
					<li class="nav-item">
						<nuxt-link class="nav-link" to="/admin/accounts">List</nuxt-link>
					</li>

					<!-- Dropdown -->
					<li class="nav-item dropdown">
						<a
							class="nav-link dropdown-toggle"
							href="#"
							id="navbardrop"
							data-toggle="dropdown"
						>
							Dropdown link
						</a>
						<div class="dropdown-menu">
							<nuxt-link class="nav-link" to="/">Home</nuxt-link>
							<nuxt-link class="dropdown-item" to="/">Another action</nuxt-link>
							<a class="dropdown-item" href="#">Link 3</a>
						</div>
					</li>
				</ul>
			</nav>
		</div>
	</header>
</template>

<style scoped></style>
