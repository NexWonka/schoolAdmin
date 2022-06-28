<script>
</script>

<div class="flex w-full flex-col p-5 static">
	<div class="grid grid-cols-1 md:grid-cols-3 gap-5 justify-items-stretch relative">
		<div class="alert alert-info shadow-lg md:col-span-3">
			<div>
				<svg
					xmlns="http://www.w3.org/2000/svg"
					fill="none"
					viewBox="0 0 24 24"
					class="stroke-current flex-shrink-0 w-6 h-6"
					><path
						stroke-linecap="round"
						stroke-linejoin="round"
						stroke-width="2"
						d="M13 16h-1v-4h-1m1-4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"
					/></svg
				>
				<span>Welcome to the admin page!</span>
			</div>
		</div>

		<div class="stats bg-base-300">
			<div class="stat">
				<div class="stat-title">Total Active Students</div>
				<div class="stat-value text-primary">89,400</div>
				<div class="stat-desc">Today</div>
			</div>
		</div>

		<div class="stats bg-base-300">
			<div class="stat">
				<div class="stat-title">Total Absent Students</div>
				<div class="stat-value text-red-500">89,400</div>
				<div class="stat-desc">Today</div>
			</div>
		</div>

		<div class="stats bg-base-300">
			<div class="stat gap-2">
				<div class="stat-title">Students Percentage</div>
				<div class="radial-progress" style="--value:70;">70%</div>
				<div class="stat-desc">Active & Non-Active Students</div>
			</div>
		</div>

		<div class="card bg-base-300">
			<figure>
				<img class="w-full" src="https://api.lorem.space/image/shoes?w=400&h=225" alt="Shoes" />
			</figure>
			<div class="card-body">
				<h2 class="card-title text-secondary animate-pulse">School Info!</h2>
				<p>Events on 17 August</p>
				<p>Please discuss with principal for more details</p>
				<div class="card-actions justify-end">
					<div class="badge badge-ghost">Updated on July, 20</div>
				</div>
			</div>
		</div>

		<div class="card bg-base-300">
			<figure>
				<img class="w-full" src="https://api.lorem.space/image/shoes?w=400&h=225" alt="Shoes" />
			</figure>
			<div class="card-body">
				<h2 class="card-title text-secondary animate-pulse">Todays Agenda</h2>
				<p>Group Meetings at 10 am</p>
				<p>Please discuss with principal for more details</p>
				<div class="card-actions justify-end">
					<div class="badge badge-ghost">Updated Today</div>
				</div>
			</div>
		</div>

		<div class="card bg-base-300">
			<figure>
				<img class="w-full" src="https://api.lorem.space/image/shoes?w=400&h=225" alt="Shoes" />
			</figure>
			<div class="card-body">
				<h2 class="card-title text-secondary animate-pulse">Something Here</h2>
				<p>Commodo nulla Lorem ad sint exercitation dolor</p>
				<div class="card-actions justify-end">
					<div class="badge badge-ghost">Updated Today</div>
				</div>
			</div>
		</div>

		<h1 class="md:col-span-3 text-primary-content font-bold">ACTIVE TUTOR & TEACHER</h1>

		<!-- TABLE  -->
		<div class="overflow-x-auto w-full md:col-span-3">
			<table class="table w-full">
				<!-- head -->
				<thead>
					<tr>
						<th>Name</th>
						<th>Job</th>
						<th>Class</th>
						<th />
					</tr>
				</thead>
				<tbody>
					<!-- row 1 -->
					<tr>
						<td>
							<div class="flex items-center space-x-3">
								<div class="avatar">
									<div class="mask mask-squircle w-12 h-12">
										<img
											src="https://source.unsplash.com/random/?people"
											alt="Avatar Tailwind CSS Component"
										/>
									</div>
								</div>
								<div>
									<div class="font-bold">Hart Hagerty</div>
									<div class="text-sm opacity-50">United States</div>
								</div>
							</div>
						</td>
						<td>
							Zemlak, Daniel and Leannon
							<br />
							<span class="badge badge-ghost badge-sm">Desktop Support Technician</span>
						</td>
						<td>Purple</td>
						<th>
							<button class="btn btn-ghost btn-xs">details</button>
						</th>
					</tr>
					<!-- row 2 -->
					<tr>
						<td>
							<div class="flex items-center space-x-3">
								<div class="avatar">
									<div class="mask mask-squircle w-12 h-12">
										<img
											src="https://source.unsplash.com/random/?people"
											alt="Avatar Tailwind CSS Component"
										/>
									</div>
								</div>
								<div>
									<div class="font-bold">Brice Swyre</div>
									<div class="text-sm opacity-50">China</div>
								</div>
							</div>
						</td>
						<td>
							Carroll Group
							<br />
							<span class="badge badge-ghost badge-sm">Tax Accountant</span>
						</td>
						<td>Red</td>
						<th>
							<button class="btn btn-ghost btn-xs">details</button>
						</th>
					</tr>
					<!-- row 3 -->
					<tr>
						<td>
							<div class="flex items-center space-x-3">
								<div class="avatar">
									<div class="mask mask-squircle w-12 h-12">
										<img
											src="https://source.unsplash.com/random/?people"
											alt="Avatar Tailwind CSS Component"
										/>
									</div>
								</div>
								<div>
									<div class="font-bold">Marjy Ferencz</div>
									<div class="text-sm opacity-50">Russia</div>
								</div>
							</div>
						</td>
						<td>
							Rowe-Schoen
							<br />
							<span class="badge badge-ghost badge-sm">Office Assistant I</span>
						</td>
						<td>Crimson</td>
						<th>
							<button class="btn btn-ghost btn-xs">details</button>
						</th>
					</tr>
					<!-- row 4 -->
					<tr>
						<td>
							<div class="flex items-center space-x-3">
								<div class="avatar">
									<div class="mask mask-squircle w-12 h-12">
										<img
											src="https://source.unsplash.com/random/?people"
											alt="Avatar Tailwind CSS Component"
										/>
									</div>
								</div>
								<div>
									<div class="font-bold">Yancy Tear</div>
									<div class="text-sm opacity-50">Brazil</div>
								</div>
							</div>
						</td>
						<td>
							Wyman-Ledner
							<br />
							<span class="badge badge-ghost badge-sm">Community Outreach Specialist</span>
						</td>
						<td>Indigo</td>
						<th>
							<button class="btn btn-ghost btn-xs">details</button>
						</th>
					</tr>
				</tbody>
			</table>
		</div>
		<!-- END TABLE  -->

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
	</div>
</div>
