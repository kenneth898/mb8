<template>
	<div class="container-fluid">
		<div class="row">

			<nav class="navbar fixed-bottom">

				<div class="container-fluid d-flex justify-content-center">


					<div class="menu d-flex justify-content-around w-100">

						<div class="nav-item d-flex flex-column align-items-center text-center column-height">
							<a :href="link" class="nav-link" rel="nofollow" target="_blank">
								<img class="nav-icon img1" src="/image/home-btn.webp" alt="Home"></a>
						</div>

						<div class="nav-item d-flex flex-column align-items-center text-center column-height">
							<a :href="link + 'sign-up'" class="nav-link" rel="nofollow" target="_blank">
								<img class="nav-icon img2" src="/image/history.webp" alt="History"></a>
						</div>

						<div class="nav-item d-flex flex-column align-items-center text-center column-height">
							<a :href="link + 'sign-up'" class="nav-link" rel="nofollow" target="_blank">
								<img class="nav-icon img3" src="/image/promo.webp" alt="Promo"></a>
						</div>
						<div class="nav-item d-flex flex-column align-items-center text-center column-height">
							<a :href="link + 'sign-up'" class="nav-link" rel="nofollow" target="_blank">
								<img class="nav-icon img4" src="/image/lucky-draw.webp" alt="lucky-draw"></a>
						</div>
						<div class="nav-item d-flex flex-column align-items-center text-center column-height">
							<a :href="link + 'sign-up'" class="nav-link" rel="nofollow" target="_blank">
								<img class="nav-icon img4" src="/image/live-chat.webp" alt="live-chat"></a>
						</div>
						<div class="nav-item d-flex flex-column align-items-center text-center column-height">
							<a :href="link + 'sign-up'" class="nav-link" rel="nofollow" target="_blank">
								<img class="nav-icon img4" src="/image/setting.webp" alt="setting"></a>
						</div>
					</div>

				</div>
			</nav>
		</div>
	</div>
</template>

<script>
import { mapGetters } from 'vuex';
export default {
	name: 'bottom',
	computed: {
		...mapGetters(['link'])
	},
	mounted() {
		// 确保只有当链接不存在时才调用 fetchLink
		this.$store.dispatch('fetchLink');
	}
};
</script>

<style scoped>
.img1 {
	width: 20%;
}

.img2 {
	width: 20%;
}

.img3 {
	width: 20%;
}

.img4 {
	width: 20%;
}

.img5 {
	width: 20%;
}

.navbar.fixed-bottom {
	background-image: url('/image/bottom-bg.webp');
	height: 5%;
	background-size: cover;
}

.nav-item {
	flex: 1;
}

.menu {
	position: relative;
	top: -8px;
	align-items: end;

}

.column-height {
	position: relative;
	height: 40%;
}

@media screen and (max-width: 2560px) {
	.navbar.fixed-bottom {
		height: 9%;
	}
}

@media screen and (max-width: 1600px) {
	.column-height {
		height: 25%;
	}
}

@media screen and (max-width: 768px) {
	.menu {
		top: -8px !important;
	}

	.img1 {
		width: 30% !important;
	}

	.img2 {
		width: 30% !important;
	}

	.img3 {
		width: 30% !important;
	}

	.img4 {
		width: 30% !important;
	}

	.img5 {
		width: 40% !important;
	}


}

@media screen and (max-width:576px) {
	.navbar.fixed-bottom {
		height: 10% !important;
	}

	.menu {
		top: -5px !important;
	}

	.img1 {
		width: 65% !important;
	}

	.img2 {
		width: 65% !important;
	}

	.img3 {
		width: 65% !important;
	}

	.img4 {
		width: 65% !important;
	}

	.img5 {
		width: 65% !important;
	}
}
</style>
