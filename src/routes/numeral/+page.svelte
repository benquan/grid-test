<script>
	import { RevoGrid } from '@revolist/svelte-datagrid';
	import { defineCustomElements } from '@revolist/revogrid/loader';
	import NumberColumnType from '@revolist/revogrid-column-numeral';

	defineCustomElements();

	const columnTypes = {
		numeric: new NumberColumnType('0,0')
	};

	const columns = [
		{
			prop: 'Num',
			name: 'My number',
			columnType: 'numeric'
		},
		{
			prop: 'Num2',
			name: 'My number2',
			columnType: 'numeric'
		}
	];
	const source = [
		{
			Num: 1000,
			Num2: 1000
		}
	];
</script>

Testing
<RevoGrid {source} {columns} {columnTypes} />
