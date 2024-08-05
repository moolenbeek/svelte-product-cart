<script lang="ts">
	import ProductCard from "$lib/productCard.svelte";

	const products : Product[] = [
		{
			id: "1",
			name: "Coffee",
			price: 5
		},
		{
			id: "2",
			name: "Banana",
			price: 1
		},
		{
			id: "3",
			name: "Apple",
			price: 2
		}
	]
</script>

<div class="container h-full mx-auto flex justify-center items-center">
	<div class="grid grid-cols-3">
		<div class="col-span-3">
			<h1>Svelte Store</h1>
		</div>
		{#each products as product}
		<ProductCard product={product} />
		{/each}
		<div class="p-2 col-span-3">
			<button class="btn variant-filled-primary">Checkout</button>
		</div>
	</div>
</div>
