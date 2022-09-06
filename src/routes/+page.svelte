<script>
	import { RevoGrid } from '@revolist/svelte-datagrid';
	import { defineCustomElements } from '@revolist/revogrid/loader';

	defineCustomElements();

	let columns = [
		{ prop: '1', name: 'Title 1' },
		{ prop: '2', name: 'Title 2' }
	];
	let source = [{ 1: 'Hello', 2: 'World' }];
</script>

Testing
<RevoGrid {source} resize="true" {columns} theme="material" />
