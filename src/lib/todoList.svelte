<script lang="ts">
	const listItems: ListItem[] = [
		{
			text: 'Banana'
		},
		{
			text: 'Oat Milk'
		},
		{
			text: 'Veggie Broth'
		}
	];
</script>

<ol class="list">
	{#each listItems as ListItem, i (i)}
		<li>
			<span>{i + 1}</span>
			<input class="input" type="text" placeholder="Input" value={ListItem.text} disabled />
			<button type="button" class="btn variant-ghost-error">x</button>
		</li>
	{/each}
	<li>
		<span>{listItems.length + 1}</span>
		<input class="input" type="text" placeholder="Input" />
		<button type="button" class="btn variant-ghost-primary">+</button>
	</li>
</ol>
