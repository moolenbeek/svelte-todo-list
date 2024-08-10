<script lang="ts">
  import { listItems, addItem, removeSelf } from "../todo";
</script>

<ol class="list">
	{#each listItems as ListItem, i (i)}
		<li>
			<span>{i + 1}</span>
			<input class="input" type="text" placeholder="Input" value={ListItem.text} disabled />
			<button type="button" class="btn variant-ghost-error" on:click={() => removeSelf()}>x</button>
		</li>
	{/each}
	<li>
		<span>{listItems.length + 1}</span>
		<input class="input" type="text" placeholder="Input" />
		<button type="button" class="btn variant-ghost-primary" on:click={() => addItem()}>+</button>
	</li>
</ol>
