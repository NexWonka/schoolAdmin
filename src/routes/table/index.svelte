<script>
</script>

<div class="flex w-full flex-col p-5 static">
	<div class="grid grid-cols-1 md:grid-cols-3 gap-5 justify-items-stretch relative">
		<h1 class="font-bold text-center md:col-span-3">Classes</h1>

		<div class="card bg-primary text-primary-content shadow-xl">
			<div class="card-body">
				<h2 class="card-title">Class A1</h2>
				<progress class="progress progress-success my-5" value="80" max="100"></progress>
				<p>Total Present 80%</p>
				<div class="card-actions justify-end">
					<a href="/table/a1">
						<button class="btn btn-secondary">Manage Attendence</button>
					</a>
				</div>
			</div>
		</div>

        <div class="card bg-primary text-primary-content shadow-xl">
			<div class="card-body">
				<h2 class="card-title">Class A2</h2>
				<progress class="progress progress-success my-5" value="100" max="100"></progress>
				<p>Total Present 100%</p>
				<div class="card-actions justify-end">
					<a href="/">
						<button class="btn btn-secondary">Manage Attendence</button>
					</a>
				</div>
			</div>
		</div>

        <div class="card bg-primary text-primary-content shadow-xl">
			<div class="card-body">
				<h2 class="card-title">Class A1</h2>
				<progress class="progress progress-success my-5" value="70" max="100"></progress>
				<p>Total Present 70%</p>
				<div class="card-actions justify-end">
					<a href="/">
						<button class="btn btn-secondary">Manage Attendence</button>
					</a>
				</div>
			</div>
		</div>

		<!-- MENU BUTTON  -->
		<div class="dropdown dropdown-top dropdown-end fixed bottom-5 right-5 md:hidden">
			<label tabindex="0" class="btn btn-primary">
				<svg
					xmlns="http://www.w3.org/2000/svg"
					class="h-6 w-6"
					fill="none"
					viewBox="0 0 24 24"
					stroke="currentColor"
					stroke-width="2"
				>
					<path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16" />
				</svg>
			</label>
			<ul
				tabindex="0"
				class="dropdown-content menu p-2 shadow bg-primary text-primary-content rounded-box w-52"
			>
				<li>
					<div class="avatar gap-3 items-center">
						<div class="mask mask-squircle w-12 h-12">
							<img src="https://source.unsplash.com/random/?people" alt="" />
						</div>
						<h1 class="w-12 truncate">Hello, Natalie Axl Rose!</h1>
						<a href="/" class="tooltip" data-tip="Logout">
							<svg
								xmlns="http://www.w3.org/2000/svg"
								class="h-6 w-6"
								fill="none"
								viewBox="0 0 24 24"
								stroke="currentColor"
								stroke-width="2"
							>
								<path
									stroke-linecap="round"
									stroke-linejoin="round"
									d="M17 16l4-4m0 0l-4-4m4 4H7m6 4v1a3 3 0 01-3 3H6a3 3 0 01-3-3V7a3 3 0 013-3h4a3 3 0 013 3v1"
								/>
							</svg>
						</a>
					</div>
				</li>
				<li><a href="/">Home</a></li>
				<li><a href="/">Table</a></li>
				<li><a href="/">Data</a></li>
				<li><a href="/">Recap</a></li>
			</ul>
		</div>
		<!-- MENU BUTTON END  -->
	</div>
</div>
