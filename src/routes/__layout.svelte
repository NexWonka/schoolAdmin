<script>
	import '../app.css';
</script>

<svelte:head>
	<meta charset="utf-8" />
	<link rel="icon" href="favicon.png" />
	<meta name="viewport" content="width=device-width, initial-scale=1" />
	<meta name="description" content="A simple school admin" />
	<title>School Admin || Home</title>
</svelte:head>

<section class="flex flex-row gap-5">
	<div
		class=" hidden md:flex flex-col p-5 bg-primary min-h-screen w-1/4 text-primary-content justify-between"
	>
		<div class="flex flex-col sticky top-5">
			<div
				class="flex flex-row justify-between p-2 px-5 transition rounded-xl cursor-pointer hover:bg-primary-focus transfrom hover:scale-95"
			>
				<a href="/"> Home </a>
				<svg
					xmlns="http://www.w3.org/2000/svg"
					class="h-6 w-6"
					fill="none"
					viewBox="0 0 24 24"
					stroke="currentColor"
					stroke-width="2"
				>
					<path stroke-linecap="round" stroke-linejoin="round" d="M17 8l4 4m0 0l-4 4m4-4H3" />
				</svg>
			</div>

			<span class="divider" />

			<a href="/table"
				class="flex flex-row justify-between p-2 px-5 transition rounded-xl cursor-pointer hover:bg-primary-focus transfrom hover:scale-95"
			>
				<p> Table </p>
				<svg
					xmlns="http://www.w3.org/2000/svg"
					class="h-6 w-6"
					fill="none"
					viewBox="0 0 24 24"
					stroke="currentColor"
					stroke-width="2"
				>
					<path stroke-linecap="round" stroke-linejoin="round" d="M17 8l4 4m0 0l-4 4m4-4H3" />
				</svg>
			</a>

			<span class="divider" />

			<div
				class="flex flex-row justify-between p-2 px-5 transition rounded-xl cursor-pointer hover:bg-primary-focus transfrom hover:scale-95"
			>
				<a href="/"> Data </a>
				<svg
					xmlns="http://www.w3.org/2000/svg"
					class="h-6 w-6"
					fill="none"
					viewBox="0 0 24 24"
					stroke="currentColor"
					stroke-width="2"
				>
					<path stroke-linecap="round" stroke-linejoin="round" d="M17 8l4 4m0 0l-4 4m4-4H3" />
				</svg>
			</div>

			<span class="divider" />

			<div
				class="flex flex-row justify-between p-2 px-5 transition rounded-xl cursor-pointer hover:bg-primary-focus transfrom hover:scale-95"
			>
				<a href="/"> Recap </a>
				<svg
					xmlns="http://www.w3.org/2000/svg"
					class="h-6 w-6"
					fill="none"
					viewBox="0 0 24 24"
					stroke="currentColor"
					stroke-width="2"
				>
					<path stroke-linecap="round" stroke-linejoin="round" d="M17 8l4 4m0 0l-4 4m4-4H3" />
				</svg>
			</div>
		</div>
		<div
			class="flex flex-row justify-between items-center fixed bottom-5 transition transform p-2 shadow-md bg-primary-focus rounded-xl hover:scale-95"
		>
			<div class="avatar gap-3 items-center">
				<div class="mask mask-squircle w-12 h-12">
					<img src="https://source.unsplash.com/random/?people" alt="" />
				</div>
				<h1>Hello, Natalie Axl Rose!</h1>
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
		</div>
	</div>

	<slot />
</section>
