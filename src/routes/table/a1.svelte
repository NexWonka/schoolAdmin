<script>
	import { onMount } from 'svelte';
	import { supabase } from '../api/supabaseClient.js';

	function getStudents() {
		return supabase.from('dummy_data').select();
	}

	let edit = 0;
	let add = 0;

	let details = {
		students_id: '',
		name: '',
		address: '',
		phone: '',
		status: '',
		status_exp: ''
	};

	async function addStudent() {
		await supabase.from('dummy_data').insert([
			{
				name: details.name,
				students_id: details.students_id,
				address: details.address,
				phone: details.phone,
				status: details.status_exp == 'Present' ? true : false,
				status_exp: details.status_exp
			}
		]);
		details = {
			students_id: '',
			name: '',
			address: '',
			phone: '',
			status: '',
			status_exp: ''
		};
		add = !add;
	}

	async function deleteAttendece(name) {
		await supabase.from('dummy_data').delete().eq('id', name);
	}

	onMount(() => {});
</script>

<div class="flex w-full flex-col p-5 static">
	<div class="grid grid-cols-1 md:grid-cols-3 gap-5 justify-items-stretch relative">
		{#await getStudents()}
			<h1>Loading...</h1>
		{:then response}
			<div class={`alert alert-warning shadow-lg col-span-3 ${edit ? 'block' : 'hidden'}`}>
				<div>
					<svg
						xmlns="http://www.w3.org/2000/svg"
						class="stroke-current flex-shrink-0 h-6 w-6"
						fill="none"
						viewBox="0 0 24 24"
						><path
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-3L13.732 4c-.77-1.333-2.694-1.333-3.464 0L3.34 16c-.77 1.333.192 3 1.732 3z"
						/></svg
					>
					<span>Warning: You are in edit mode, any changes that you make can't be reverse!</span>
					<div class="flex-none">
						<button
							class="btn btn-sm btn-secondary"
							on:click={() => {
								edit = !edit;
							}}>Exit</button
						>
					</div>
				</div>
			</div>

			<div class="overflow-x-auto md:col-span-3">
				<table class="table w-full">
					<thead>
						<tr>
							<th>Students ID</th>
							<th>Name</th>
							<th>Address</th>
							<th>Phone</th>
							<th>Status</th>
							<th />
							{#if edit}
								<th>Action</th>
							{/if}
						</tr>
					</thead>

					<tbody>
						{#each response.data as student}
							<tr>
								<th>{student.students_id}</th>
								<th>{student.name}</th>
								<th>{student.address}</th>
								<th>{student.phone}</th>
								<th>{student.status_exp}</th>
								<th>
									{#if student.status}
										<svg
											xmlns="http://www.w3.org/2000/svg"
											class="h-6 w-6 text-green-500"
											fill="none"
											viewBox="0 0 24 24"
											stroke="currentColor"
											stroke-width="2"
										>
											<path stroke-linecap="round" stroke-linejoin="round" d="M5 13l4 4L19 7" />
										</svg>
									{:else}
										<svg
											xmlns="http://www.w3.org/2000/svg"
											class="h-6 w-6 text-red-500"
											fill="none"
											viewBox="0 0 24 24"
											stroke="currentColor"
											stroke-width="2"
										>
											<path
												stroke-linecap="round"
												stroke-linejoin="round"
												d="M6 18L18 6M6 6l12 12"
											/>
										</svg>
									{/if}
								</th>
								{#if edit}
									<th>
										<button class="btn btn-sm" on:click={deleteAttendece(student.id)}>
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
													d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16"
												/>
											</svg>
										</button>
									</th>
								{/if}
							</tr>
						{/each}
					</tbody>
				</table>
			</div>

			<div class="col-span-3">
				<button
					class="btn btn-primary"
					on:click={() => {
						add = !add;
					}}>ADD STUDENTS</button
				>
				<button
					class="btn btn-outline"
					on:click={() => {
						edit = !edit;
					}}
				>
					EDIT ATTENDENCE
				</button>
			</div>
		{/await}

		<div
			class={`flex flex-col col-span-3 gap-5 bg-base-300 p-5 rounded-xl ${
				add ? 'block' : 'hidden'
			}`}
		>
			<div class="col-span-3">
				<h1>STUDENTS ID</h1>
			</div>
			<div class="col-span-3">
				<input
					type="text"
					placeholder="Type here"
					class="input input-bordered w-full"
					required
					bind:value={details.students_id}
				/>
			</div>
			<div class="col-span-3">
				<h1>NAME</h1>
			</div>
			<div class="col-span-3">
				<input
					type="text"
					placeholder="Type here"
					class="input input-bordered w-full"
					required
					bind:value={details.name}
				/>
			</div>
			<div class="col-span-3">
				<h1>ADDRESS</h1>
			</div>
			<div class="col-span-3">
				<input
					type="text"
					placeholder="Type here"
					class="input input-bordered w-full"
					required
					bind:value={details.address}
				/>
			</div>
			<div class="col-span-3">
				<h1>PHONE</h1>
			</div>
			<div class="col-span-3">
				<input
					type="text"
					placeholder="Type here"
					class="input input-bordered w-full"
					required
					bind:value={details.phone}
				/>
			</div>
			<div class="col-span-3">
				<h1>STATUS</h1>
			</div>
			<div class="col-span-3">
				<select class="select w-full" bind:value={details.status_exp}>
					<option disabled selected>Attendence Status</option>
					<option>Present</option>
					<option>Sick</option>
					<option>Alpha</option>
					<option>Away</option>
				</select>
			</div>
			<div class="flex col-span-3 items-end justify-end">
				<button class="btn btn-primary" on:click={addStudent}> Confirm </button>
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
