<script lang="ts">
	const LitstItems: ListItem[] = [
		{
			id: '1',
			text: 'Oat Milk'
		},
		{
			id: '2',
			text: 'Eggs'
		}
	];
</script>

<div class="container h-full mx-auto flex justify-center items-center">
	<div class="grid">
		<h1>Todo</h1>

		<ol class="list">
			{#each LitstItems as ListItem}
			<li>
				<span>{ListItem.id}.</span>
				<span class="flex-auto">{ListItem.text}</span>
			</li>
			{/each}
		</ol>

		<button class="my-4 p-2 rounded variant-glass-primary" on:click={() => console.log('add')}>Add</button>
	</div>
</div>
