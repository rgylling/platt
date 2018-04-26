<template>
	<div class="products">
		<div class="desktop-only">
			<div class="product-title">
				<h5 class="product-title-inner">Product Markets</h5>
			</div>
			<ul class="product-list">
				<li v-for="(product, index) in products" class="product-list-item">
					<div class="product-list-image-container">
						<img class="product-list-image" :src="product.img">
					</div>
					<div class="product-list-text">
						{{product.label}}
					</div>
				</li>
			</ul>
		</div>
		<div class="mobile-products mobile-only">
			<ul class="mobile-products-inner">
				<li class="mobile-item">
					<a class="mobile-item-button"><img class="mobile-item-image" src="../assets/ic/green/ic_line_style.png"></a>
					<div class="mobile-item-name">Categories</div>
				</li>
				<li class="mobile-item">
					<a class="mobile-item-button"><img class="mobile-item-image" src="../assets/ic/green/ic_search.png"></a>
					<div class="mobile-item-name">Search</div>

				</li>
				<li class="mobile-item">
					<a class="mobile-item-button"><img class="mobile-item-image" src="../assets/ic/green/ic_scanner.png"></a>
					<div class="mobile-item-name">Scan</div>
				</li>
			</ul>
		</div>
	</div>

</template>

<script>
	import dataComm from '../assets/img/datacomm.png'
	import hvac from '../assets/img/hvac.png'
	import industrial from '../assets/img/industrial.png'
	import lighting from '../assets/img/lighting.png'
	import energy from '../assets/img/energy.png'
	import utility from '../assets/img/utility.png'

	export default {
		name: 'AppProducts',
		data: function () {
			return {
				products: [
					{
						label: 'DataComm',
						img: dataComm
					},
					{
						label: 'HVAC',
						img: hvac
					},
					{
						label: 'Industrial',
						img: industrial
					},
					{
						label: 'Lighting',
						img: lighting,
					},
					{
						label: 'Energy Efficiency',
						img: energy
					},
					{
						label: 'Utility',
						img: utility
					}
				]
			}
		}
	}
</script>

<style lang="scss">
	@import '../styles/common.scss';
	@import '../styles/responsive.scss';

	.products {
		margin-bottom: 20px;
	}
	.product-title {
		text-align:center;
		padding: 20px 0;
	}

	.product-title-inner {
		font-weight: 600;
		letter-spacing:1.5px;
	}

	.product-list {
		display: flex;
		flex-wrap: wrap;
		flex-direction: row;
		justify-content: flex-end
	}

	.product-list-item {
		display: block;
		flex: 1 0 10%;
		text-align: center;
		background-color: white;
		margin-right: 25px;
		box-shadow: $box-shadow;
	}

	.product-list-item:nth-child(6n) {
		margin-right: 0;

	}

	.product-list-item:nth-child(6n + 1) {
		margin-left: 0;

	}

	.product-list-item:last-child {
		margin-right: 0;

	}

	.product-list-text {
		padding: 25px 20px;
		font-weight: 600;
	}

	.product-list-image {
		width: 100%;
	}

	.mobile-products-inner {
		padding: 50px;
		display:flex;
		justify-content: space-between;
		text-align: center;
	}

	.mobile-item-button {
		background-color: #fff;
		border-radius: 100%;
		width: 65px;
		height: 65px;
		margin: 0 auto;
		border: 1px solid #ccc;
		display: inline-block;
		text-align: center;
		outline: none;
		box-shadow: inset 0 -2px 0 rgba(0,0,0,.4);
		cursor: pointer;
	}

	.mobile-item-image {
		top: 18px;
		left: 1px;
		position: relative;
	}

	@media screen and (max-width: $mobile-size) {
		.products {
			margin-bottom: 0px;
		}
	}

</style>
