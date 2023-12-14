<script lang="ts">
	let count: number = 0;
	const increment = () => {
		count += 1;
	};
</script>

<div class="flex flex-col gap-4 items-center">
	<button
		on:click={increment}
		class="bg-gray-200 p-2 rounded-xl focus: border-2 focus:border-red-300 text-lg"
	>
		Increase
	</button>
	<span class="text-base">{count}</span>
</div>
