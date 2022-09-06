<script>
	import { RevoGrid } from '@revolist/svelte-datagrid';
	import { defineCustomElements } from '@revolist/revogrid/loader';
	import SelectTypePlugin from '@revolist/revogrid-column-select';

	defineCustomElements();
	const columns = [
		{
			prop: 'name',
			name: 'First',
			size: 150,
			columnType: 'select',
			source: ['According', 'Source']
		},
		{
			prop: 'details',
			name: 'Second column',
			size: 200
		}
	];
	// rows collection
	const source = [
		{
			name: 'Source',
			details: 'Item description'
		}
	];
	// register column type
	const columnTypes = { select: new SelectTypePlugin() };
</script>

Testing
<RevoGrid {source} {columns} {columnTypes} />
