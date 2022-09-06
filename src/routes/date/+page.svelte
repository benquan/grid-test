<script>
	import { RevoGrid } from '@revolist/svelte-datagrid';
	import { defineCustomElements } from '@revolist/revogrid/loader';
	import Plugin from '@revolist/revogrid-column-date';

	defineCustomElements();

	const columns = [{ prop: 'name', columnType: 'date' }];
	const source = [{ name: '2020-08-24' }, { name: '2022-08-24' }];

	// register column type
	const columnTypes = { date: new Plugin() };
</script>

Testing
<RevoGrid {source} {columns} {columnTypes} />
