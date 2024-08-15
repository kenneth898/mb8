<template>
	<div style="padding-top: 10px;" class="main-col container">
		<div v-for="(image, index) in images" :key="index" class="col">
			<img :src="`/menu-game/${image.fileName}.webp`" :alt="image.fileName" class="img-fluid">
			<p style="margin-bottom: 10px;">{{ $t('menu.play') }}</p>
		</div>
	</div>
</template>

<script>
export default {
	name: 'Menu1',
	data() {
		return {
			images: [
				{ fileName: '1-tanzania-king' },
				{ fileName: '2-candy-party' },
				{ fileName: '3-legend-slot-onimaru-cp-fc' },
				{ fileName: '4-legend-slot-musashi-cp-fc' },
				{ fileName: '5-durian-king' },
				{ fileName: '6-thai-lucky' },
				{ fileName: '7-colour-alchemy' },
				{ fileName: '8-trade-wars' },
				{ fileName: '9-gems-rush' },
				{ fileName: '10-gods-of-olympus' },
				{ fileName: '11-beauty-contest' },
				{ fileName: '12-dragon-jewels' },
				{ fileName: '13-golden-temple' },
				{ fileName: '14-life' },
				{ fileName: '15-magic-box' },
				{ fileName: '16-mr-fortune' },
				{ fileName: '17-meow-meow' },
				{ fileName: '18-lucky-7' },
				{ fileName: '19-where-is-my-monkey' },
				{ fileName: '20-samurai-wars' },
				{ fileName: '21-happy-road' },
				{ fileName: '22-feed-the-zombie' },
				{ fileName: '23-burn-the-office' },
				{ fileName: '24-all-you-can-eat' },
				{ fileName: '25-tv-worlds' },
				{ fileName: '26-strange-encounter' },
				{ fileName: '27-sos' },
				{ fileName: '28-oh-crap' },
				{ fileName: '29-pon-pon' },
				{ fileName: '30-lullababy' },
				{ fileName: '31-talent-night' },
				{ fileName: '32-spell-craft' },
				{ fileName: '33-steampunk-100_sqre' },
				{ fileName: '34-thai-street-food' },

			]
		};
	}
};
</script>

<style scoped>
.main-col {
	display: grid;
	grid-template-columns: repeat(6, 1fr);
	justify-items: center;
	gap: 0.5rem;
	text-align: center;
	text-align: -webkit-center;
}

@media screen and (max-width: 768px) {
	.main-col {
		grid-template-columns: repeat(3, 1fr);
	}
}

a {
	text-decoration: none;
}

p {
	padding: 5px;
	margin-top: 5px;
	width: 100%;
	color: #fff;
	background-image: url('/image/play-btn.webp');
	padding: 3px 0;
	margin-top: 8px;
	font-size: 11px;
	background-color: transparent !important;
	background-size: 100% 100%;
	border: 0;
}

img {
	border-radius: 10px;
	border: 1px solid #fff;
	background-color: #fff;
}
</style>
