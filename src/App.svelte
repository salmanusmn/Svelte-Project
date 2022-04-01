<script>
	import data from "./data.json";

	let posts = data.data;
</script>

<main class="flex flex-col justify-center items-center h-screen space-y-4">
	{#each posts as post}
		<div class="card w-96 bg-base-100 shadow-xl">
			<div class="card-body">
				<h2 class="card-title">{post.author}</h2>
				<p>{post.post}</p>
			</div>
		</div>
	{/each}
</main>

<style>
</style>
