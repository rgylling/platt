<template>
	<div class="search-container">
		<input class="search"
		type="text"
		v-model="search"
		@input="onChange"
		placeholder="What are you looking for?"
		/>
		<ul
		v-show="isOpen"
		class="autocomplete-results">
			<li
			v-for="(result, i) in results"
			:key="i"
			@click="setResult(result)"
			class="autocomplete-result">
			{{ result }}
			</li>
		</ul>
	</div>
</template>

<script>
import request from 'superagent'

	export default {
		name: 'AppSearch',
		mounted() {
			this.getData();
		},
		data() {
			return {
				search: '',
				results: [],
				data: [],
				isOpen: false
			}
		},
		methods: {
			onChange() {
				this.isOpen = true;
				this.filterResults();
			},
			filterResults() {
				if(this.data.length) {
					this.results = this.data.filter(item => item.toLowerCase().indexOf(this.search.toLowerCase()) > -1);
				}

			},
			setResult(result) {
				this.search = result;
				this.isOpen = false;
			},
			getData() {
				request
				.get('http://jsonplaceholder.typicode.com/users')
				.end((err, response) => {
					var json = JSON.parse(response.text);
					this.data = json.map(x => x.name);
				})
			}
		}
	}
</script>

<style lang="scss">
	@import '../styles/common.scss';
	.autocomplete-results {
		padding: 0;
		margin: 0;
		border: 1px solid #eeeeee;
		background-color:white;
		height: 120px;
		overflow: auto;
		position: absolute;
		width: 99.5%;
		z-index: 3;
	}

	.autocomplete-result {
		list-style: none;
		text-align: left;
		padding: 4px 2px;
		cursor: pointer;
	}

	.autocomplete-result:hover {
		background-color: #4AAE9B;
		color: white;
	}
	.search-container {
		padding: 10px 3px 5px;
		position: relative;
	}
	.search {
		width: 100%;
		font-size: 16px;
		padding: 15px;
		border-radius: 3px;
		background-image: url('../assets/ic/black/ic_search.png');
		background-repeat: no-repeat;
		background-position: right center;
		background-origin: content-box;
		outline: none;
	}
</style>
