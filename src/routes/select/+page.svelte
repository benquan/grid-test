<script>
	import { RevoGrid } from '@revolist/svelte-datagrid';
	import { defineCustomElements } from '@revolist/revogrid/loader';
	import SelectTypePlugin from '@revolist/revogrid-column-select';

	defineCustomElements();

	const columns = [
		{
			prop: 'name',
			labelKey: 'label',
			valueKey: 'value',
			source: [
				{ label: 'According', value: 'a' },
				{ label: 'Over', value: 'b' },
				{ label: 'Source', value: 's' }
			],
			columnType: 'select' // column type specified as 'select'
		}
	];
	const source = [{ name: 'New item' }, { name: 'New item 2' }];

	// register column type
	const columnTypes = { select: new SelectTypePlugin() };
</script>

Testing
<RevoGrid {source} {columns} {columnTypes} />
