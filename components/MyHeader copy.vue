<template>
	<header class="mb-auto">
		<div>
			<nav class="navbar navbar-expand-lg bg-primary">
				<div class="container-fluid">
					<a class="navbar-brand" href="#">Nuxt 3+Bootstrap5+Bootswatch</a>
					<button
						class="navbar-toggler bg-light"
						type="button"
						data-bs-toggle="collapse"
						data-bs-target="#navbarSupportedContent"
						aria-controls="navbarSupportedContent"
						aria-expanded="false"
						aria-label="Toggle navigation"
					>
						<span class="navbar-toggler-icon"></span>
					</button>
					<div class="collapse navbar-collapse" id="navbarSupportedContent">
						<ul class="navbar-nav me-auto mb-2 mb-lg-0">
							<li class="nav-item">
								<nuxt-link class="nav-link" to="/">Home</nuxt-link>
							</li>
							<li class="nav-item">
								<nuxt-link class="nav-link" to="/admin/accounts"
									>List</nuxt-link
								>
							</li>
							<li class="nav-item dropdown">
								<a
									class="nav-link dropdown-toggle"
									href="#"
									id="navbarDropdown"
									role="button"
									data-bs-toggle="dropdown"
									aria-expanded="false"
								>
									Dropdown
								</a>
								<ul class="dropdown-menu" aria-labelledby="navbarDropdown">
									<li>
										<nuxt-link class="nav-link" to="/">Home</nuxt-link>
									</li>
									<li>
										<nuxt-link class="dropdown-item" to="/"
											>Another action</nuxt-link
										>
									</li>
									<li><hr class="dropdown-divider" /></li>
									<li>
										<nuxt-link class="dropdown-item" to="/"
											>omething else here</nuxt-link
										>
									</li>
								</ul>
							</li>
						</ul>
					</div>
				</div>
			</nav>
		</div>
	</header>
</template>

<style scoped></style>
