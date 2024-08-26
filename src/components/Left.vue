<template>
	<div class="container-fluid">
		<div class="col-12 ">
			<div class="row ">


				<div class="mobile">
					<a href="https://www.atascasinobet1.com/sign-up" rel="nofollow">
						<img width="100%" src="/image/daily_top_up_bonus.webp" alt="daily_top_up_bonus">
					</a>
				</div>
				<div class="bg_img">
					<div class="desktop">
						<a href="https://www.atascasinobet1.com/sign-up" rel="nofollow">
							<img width="100%" src="/image/atas_one_stop_platform.webp" alt="atas_one_stop_platform">
						</a>
					</div>


					<img width="100%" src="/image/logo1.webp" style="padding-top: 10px;" alt="gamelicense">



					<div class="table">
						<table class="table  table-bordered">
							<thead>
								<tr>
									<th class="table_title" colspan="5">
										{{ $t('LiveTransaction.LiveTransaction') }}
										<div class="live">
											<p style="margin: 0;">LIVE <span class="live_span"></span></p>
										</div>
									</th>
								</tr>
								<tr>
									<th class="topup" colspan="2">{{ $t('LiveTransaction.deposit') }}</th>
									<th class="withdraw" colspan="3">
										{{ $t('LiveTransaction.withdraw') }}</th>
								</tr>
							</thead>
							<tbody>
								<tr v-for="(item, index) in tableData" :key="index">
									<td style="padding: 1px;">{{ item.topUpId }}</td>
									<td style="padding: 1px;color: #D0AD25;">{{ item.topUpAmount }}</td>
									<td style="padding:1px;">{{ item.withdrawId }}</td>
									<td style="padding: 1px;color: #D0AD25;">{{ item.withdrawAmount }}</td>
									<td style="padding: 1px;">{{ item.game }}</td>
								</tr>
							</tbody>
						</table>
					</div>



					<div class="srceen_mobile">

						<!--button bg-->
						<div style="padding-top: 10px;" class="btn_bg">
							<a href="https://www.atascasinobet1.com/sign-up" rel="nofollow">
								<img width="100%" src="/image/btn-bg.webp" alt="btn_bg">
							</a>

							<div style="position: absolute; bottom: 8px;" class="row">
								<div class="col-6 btn_left">
									<a href="https://www.atascasinobet1.com/sign-up" rel="nofollow">
										<img width="95%" src="/image/share-btn.gif" alt="share">
									</a>
								</div>
								<div class="col-6 btn_right">
									<a href="https://www.atascasinobet1.com/sign-up" rel="nofollow">
										<img width="95%" src="/image/downline.gif" alt="downline">
									</a>
								</div>
								<div style="padding-top: 5px; padding-right: 3px;" class="col-6 btn_left">
									<a href="https://www.atascasinobet1.com/sign-up" rel="nofollow">
										<img width="94%" src="/image/copy.gif" alt="copy">
									</a>
								</div>
								<div style="padding-top: 5px; " class="col-6 btn_right">
									<a href="https://www.atascasinobet1.com/sign-up" rel="nofollow">
										<img width="94%" src="/image/more.gif" alt="more">
									</a>
								</div>
							</div>
						</div>

						<!--live now-->
						<a href="https://www.atascasinobet1.com/sign-up" rel="nofollow">
							<img width="100%" src="/image/live-now.webp" style="padding-top: 10px;" alt="live now">
						</a>
					</div>

					<div class="">

					</div>


				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: 'Left',
	data() {
		return {
			tableData: this.generateInitialData(),
			isDragging: false,
			startX: 0,
			scrollLeft: 0
		};
	},
	mounted() {
		this.startUpdatingData();
	},
	methods: {
		startDrag(e) {
			this.isDragging = true;
			this.startX = e.pageX - this.$refs.carousel.offsetLeft;
			this.scrollLeft = this.$refs.carousel.scrollLeft;
			this.$refs.carousel.style.cursor = 'grabbing';
		},
		endDrag() {
			this.isDragging = false;
			this.$refs.carousel.style.cursor = 'grab';
		},
		onDrag(e) {
			if (!this.isDragging) return;
			e.preventDefault();
			const x = e.pageX - this.$refs.carousel.offsetLeft;
			const walk = (x - this.startX) * 2; // Adjust scroll speed
			this.$refs.carousel.scrollLeft = this.scrollLeft - walk;
		},
		generateInitialData() {
			return Array.from({ length: 5 }, () => this.createRandomEntry());
		},
		startUpdatingData() {
			setInterval(() => {
				this.updateData();
			}, 10000); // 每5秒更新一次数据
		},
		createRandomEntry() {
			const generateRandomId = () => `60******${Math.floor(Math.random() * 1000).toString().padStart(3, '0')}`;
			const generateRandomAmount = (max) => `RM${(Math.random() * max).toFixed(2)}`;
			const games = ['KISS918', 'RICHGAMING', 'JILI'];

			return {
				topUpId: generateRandomId(),
				topUpAmount: generateRandomAmount(50), // 最高RM50
				withdrawId: generateRandomId(),
				withdrawAmount: generateRandomAmount(2000), // 最高RM500
				game: games[Math.floor(Math.random() * games.length)],
			};
		},
		updateData() {
			this.tableData = Array.from({ length: 5 }, () => this.createRandomEntry());
		}
	}
};
</script>

<style scoped>
@media screen and (max-width:1000px) {
	.table tr {
		font-size: 7px !important;

	}

	.table_title {
		font-size: 10px !important;
	}
}

.bg_img {
	height: 100%;
}

@media screen and (max-width:768px) {
	.bg_img {
		padding-bottom: 0px;
	}

	.table tr {
		font-size: 9px !important;
	}

	.table_title {
		font-size: 12px;

	}
}


.carousel {
	padding-top: 10px;
}


.btn_bg {
	position: relative;
	padding-top: 10px;
}

.btn_left {
	text-align-last: end;
	padding-right: 0px;
}

.btn_right {
	text-align-last: start;
	padding-left: 0px;
}

.desktop {
	padding-top: 10px;
}

.mobile {
	display: none;
	padding: 0;
}


@media screen and (max-width:768px) {
	.desktop {
		display: none;
	}

	.mobile {
		display: block;
	}

	.bg_test {

		width: 100% !important;
	}
}

.bonus {
	padding-top: 10px;
}

.table {
	padding-top: 10px;
	margin: 0px;

}

.table tr {
	font-size: 9px;

}

.table th {
	background-color: black;
}

.table_title {
	color: #D3AB22;
	font-size: 12px;

}

.live {
	display: inline;
	float: right;
	margin: 0;
	background-color: red;
	color: white;

	padding: 0px 5px 0px 5px;
	border-radius: 5px;
}

.live_span {
	display: block;
	width: 8px;
	height: 8px;
	background: #fff;
	float: right;
	border-radius: 10px;
	margin: 5px 1px 0 3px;
}

tbody tr td {
	background-color: black;
	color: #fff;
}

@keyframes blink {
	0% {
		opacity: 1;
	}

	50% {
		opacity: 0;
	}

	100% {
		opacity: 1;
	}
}

.live {
	animation: blink 1s infinite;
	/* 动画持续时间设置为1秒并无限次循环 */
}

.topup {
	padding-bottom: 1px;
	padding-top: 1px;
	padding-left: 5px;
	background: radial-gradient(circle, rgba(79, 255, 69, 1) 0%, rgba(29, 75, 31, 1) 100%);
	color: #fff;
}

.withdraw {
	padding-bottom: 1px;
	padding-top: 1px;
	padding-left: 5px;
	background: radial-gradient(circle, rgba(254, 255, 26, 1) 0%, rgba(0, 0, 0, 1) 100%);
	color: white;
}

.bg_test {
	align-content: center;
	background-image: url(/image/right_bg2.webp);
	background-repeat: round;
	text-align: -webkit-center;
	width: 100%;
	margin-top: 10px;
	border-radius: 15px;
	padding-bottom: 10px;
	margin-bottom: 10px;
}

.right2 {
	margin-top: 25px;
	background-color: #FFF;
	border-radius: 10px;
	align-items: center;
	text-align: center;
	width: 95%;
}

.sportlive_col {
	padding: 26px 0px 10px 18px;
	text-align: -webkit-center;
	position: absolute;
}

.sportlive_text {
	font-size: 21px;
	color: #258D2D;
	font-family: digital-7;
}

.betnow {
	display: block;
	background: #4caf50;
	color: #fff;
	padding: 8px 0;
	line-height: 1;
	width: 72px;
	text-align: center;
	border-radius: 4px;
	margin: 5px auto 0;
	margin-bottom: 10px;
	text-decoration: none;
}

.showmore {
	background-color: #EEE;
	color: #000;
	text-align: center;
	padding: 8px;
	font-size: 13px;
	line-height: 1;
	border-radius: 5px;
	width: 95%;
	box-shadow: 0 0 3px rgb(0 0 0 / 30%);
	border: 1px solid #ccc;
	cursor: pointer;
	text-decoration: none;
}

a {
	text-decoration: none;
}

.showmore_col {
	padding-top: 10px;
	margin-bottom: 10px;
}

@media screen and (max-width:770px) {


	.text_sportlive {
		font-size: 15px !important;
	}

	.betnow {
		font-size: 10px;
	}


}



@media screen and (max-width:426px) {


	.text_sportlive {
		font-size: 14px !important;
	}
}

.bonus {
	display: none;
}

@media screen and (max-width:768px) {
	.bonus {
		display: block;
	}

	.desktop {
		display: none;
	}
}

.carousel-indicators .single-dot {
	width: 12px;
	height: 12px;
	background-color: #fff;
	border-radius: 50%;
	cursor: pointer;

}

.carousel-indicators li {
	width: 12px;
	height: 12px;
	background-color: #fff;
	border-radius: 50%;
	cursor: pointer;
	transition: background-color 0.3s;
}

.carousel-indicators li.active {
	background-color: #fffcfc;
}

/* Remove default list numbering */
.carousel-indicators ol {
	list-style: none;
	padding: 0;
	margin: 0;
}

.carousel-indicators li::before {
	content: none;
}

.carousel-indicators li::marker {
	display: none !important;
	color: rgba(0, 0, 0, 0);
}

.carousel-indicators {
	z-index: 1;
}
</style>