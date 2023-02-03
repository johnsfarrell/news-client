<script>
	import { AdvancedRating, Rating } from 'flowbite-svelte';

	// table
	import {
		Table,
		TableBody,
		TableBodyCell,
		TableBodyRow,
		TableHead,
		TableHeadCell,
		TableSearch
	} from 'flowbite-svelte';
	let searchTerm = '';
	let items = [
		{ id: 1, maker: 'Toyota', type: 'ABC', make: 2017 },
		{ id: 2, maker: 'Ford', type: 'CDE', make: 2018 },
		{ id: 3, maker: 'Volvo', type: 'FGH', make: 2019 },
		{ id: 4, maker: 'Saab', type: 'IJK', make: 2020 }
	];
	$: filteredItems = items.filter(
		(item) => item.maker.toLowerCase().indexOf(searchTerm.toLowerCase()) !== -1
	);
</script>

<div>
	<AdvancedRating
		labelClass={'text-sm text-gray-500 dark:text-gray-400'}
		rightLabelClass={'text-sm text-gray-500 dark:text-gray-400'}
		ratings={[
			{ label: '5 star', rating: 70 },
			{ label: '4 star', rating: 17 },
			{ label: '3 star', rating: 8 },
			{ label: '2 star', rating: 4 },
			{ label: '1 star', rating: 1 }
		]}
	>
		<span slot="rating">
			<Rating total={5} rating={3.21}>
				<p slot="text" class="ml-2 text-sm font-medium text-gray-500 dark:text-gray-400">
					3.21 out of 5 from 1,745 analyst ratings
				</p>
			</Rating>
		</span>
	</AdvancedRating>
	<hr class="h-px my-8 bg-gray-200 border-0 dark:bg-gray-700" />
	<TableSearch placeholder="Search by analyst" hoverable={true} bind:inputValue={searchTerm}>
		<TableHead>
			<TableHeadCell>Analyst</TableHeadCell>
			<TableHeadCell>Rating</TableHeadCell>
			<TableHeadCell>Total Analyses</TableHeadCell>
			<TableHeadCell>
				<span class="sr-only"> Details </span>
			</TableHeadCell>
		</TableHead>
		<TableBody tableBodyClass="divide-y">
			{#each filteredItems as item}
				<TableBodyRow>
					<TableBodyCell>{item.id}</TableBodyCell>
					<TableBodyCell>{item.maker}</TableBodyCell>
					<TableBodyCell>{item.type}</TableBodyCell>
					<TableBodyCell>
						<a href="/tables" class="font-medium text-blue-600 hover:underline dark:text-blue-500">
							Details
						</a>
					</TableBodyCell>
				</TableBodyRow>
			{/each}
		</TableBody>
	</TableSearch>
</div>
