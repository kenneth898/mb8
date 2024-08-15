<template>
	<div class="container-fluid">
		<div class="col-12">
			<div class="row bg">
				<div style="padding: 0px;" class="col-sm-12 col-md-3">
					<!--left-->
					<div class="left">
						<div class="leftright_bg">
							<Left />
						</div>
					</div>
				</div>

				<div style="padding: 10px;" class="col-sm-12 col-md-6 mobile_col2 center_col">
					<!--main-->
					<div style="padding-bottom: 10px;" class="nav nav-pills">
						<a style="padding: 0px; border-radius: 0; padding-bottom: 10px;"
							v-for="(item, index) in menuItems" :key="index"
							:class="['nav-link', { active: activeIndex === index }]"
							@click="setActive(index, item.componentId)">
							<img :src="activeIndex === index ? item.activeSrc : item.inactiveSrc" :alt="item.name"
								class="img-fluid" />
						</a>
					</div>

					<div :id="menuItems[0].componentId">
						<component :is="currentComponent"></component>
					</div>

					<div style="padding-bottom: 70px;" class="content" :id="menuItems[1].componentId">
						<Content />
					</div>

				</div>

				<div style="padding: 0px;" class="col-sm-12 col-md-3 mobile_col">
					<!--right-->
					<div class="right">
						<div class="right_bg">
							<Right />
						</div>
					</div>
				</div>


				<div class=" icon_col">
					<div class="icon">
						<!--Telegram icon-->
						<a href="https://t.me/atas77channel" rel="nofollow" target=" _blank"> <span
								class="chaty-icon channel-icon-Telegram">
								<span class="chaty-svg">
									<svg width="39" height="39" viewBox="0 0 39 39" fill="none"
										xmlns="http://www.w3.org/2000/svg">
										<circle class="color-element" cx="19.4395" cy="19.4395" r="19.4395"
											fill="#3E99D8">
										</circle>
										<path d="M3.56917 -2.55497e-07L0 6.42978L7.5349 1.87535L3.56917 -2.55497e-07Z"
											transform="translate(13.9704 24.6145)" fill="#E0E0E0">
										</path>
										<path
											d="M20.8862 0.133954C20.754 0 20.4897 0 20.2253 0L0.396574 8.03723C0.132191 8.17118 0 8.43909 0 8.707C0 8.97491 0.132191 9.24282 0.396574 9.37677L17.5814 17.414C17.7136 17.414 17.7136 17.414 17.8458 17.414C17.978 17.414 18.1102 17.414 18.1102 17.28C18.2424 17.1461 18.3746 17.0121 18.5068 16.7442L21.1506 0.669769C21.1506 0.535815 21.1506 0.267908 20.8862 0.133954Z"
											transform="translate(7.36069 10.9512)" fill="white">
										</path>
										<path d="M13.8801 0L0 11.52V19.4233L3.70136 13.2614L13.8801 0Z"
											transform="translate(13.9704 11.6208)" fill="#F2F2F2">
										</path>
									</svg>
								</span>
							</span>
						</a>

						<!--Twitter icon-->
						<a style="background-color: white; border-radius: 40px; text-align: -webkit-center;"
							href=" https://x.com/atascasinomy" rel="nofollow" target=" _blank"><svg
								xmlns="http://www.w3.org/2000/svg" width="20" height="39" fill="currentColor"
								class="bi bi-twitter" viewBox="0 0 16 16">
								<path
									d="M5.026 15c6.038 0 9.341-5.003 9.341-9.334q.002-.211-.006-.422A6.7 6.7 0 0 0 16 3.542a6.7 6.7 0 0 1-1.889.518 3.3 3.3 0 0 0 1.447-1.817 6.5 6.5 0 0 1-2.087.793A3.286 3.286 0 0 0 7.875 6.03a9.32 9.32 0 0 1-6.767-3.429 3.29 3.29 0 0 0 1.018 4.382A3.3 3.3 0 0 1 .64 6.575v.045a3.29 3.29 0 0 0 2.632 3.218 3.2 3.2 0 0 1-.865.115 3 3 0 0 1-.614-.057 3.28 3.28 0 0 0 3.067 2.277A6.6 6.6 0 0 1 .78 13.58a6 6 0 0 1-.78-.045A9.34 9.34 0 0 0 5.026 15" />
							</svg></a>

						<!--whatsapp icon-->
						<a href="https://rebrand.ly/ATASxSEO2P" rel="nofollow" target="_blank">
							<span class="chaty-icon channel-icon-Whatsapp">
								<span class="chaty-svg">
									<svg width="39" height="39" viewBox="0 0 39 39" fill="none"
										xmlns="http://www.w3.org/2000/svg">
										<circle class="color-element" cx="19.4395" cy="19.4395" r="19.4395"
											fill="#49E670">
										</circle>
										<path
											d="M12.9821 10.1115C12.7029 10.7767 11.5862 11.442 10.7486 11.575C10.1902 11.7081 9.35269 11.8411 6.84003 10.7767C3.48981 9.44628 1.39593 6.25317 1.25634 6.12012C1.11674 5.85403 2.13001e-06 4.39053 2.13001e-06 2.92702C2.13001e-06 1.46351 0.83755 0.665231 1.11673 0.399139C1.39592 0.133046 1.8147 1.01506e-06 2.23348 1.01506e-06C2.37307 1.01506e-06 2.51267 1.01506e-06 2.65226 1.01506e-06C2.93144 1.01506e-06 3.21063 -2.02219e-06 3.35022 0.532183C3.62941 1.19741 4.32736 2.66092 4.32736 2.79397C4.46696 2.92702 4.46696 3.19311 4.32736 3.32616C4.18777 3.59225 4.18777 3.59224 3.90858 3.85834C3.76899 3.99138 3.6294 4.12443 3.48981 4.39052C3.35022 4.52357 3.21063 4.78966 3.35022 5.05576C3.48981 5.32185 4.18777 6.38622 5.16491 7.18449C6.42125 8.24886 7.39839 8.51496 7.81717 8.78105C8.09636 8.91409 8.37554 8.9141 8.65472 8.648C8.93391 8.38191 9.21309 7.98277 9.49228 7.58363C9.77146 7.31754 10.0507 7.1845 10.3298 7.31754C10.609 7.45059 12.2841 8.11582 12.5633 8.38191C12.8425 8.51496 13.1217 8.648 13.1217 8.78105C13.1217 8.78105 13.1217 9.44628 12.9821 10.1115Z"
											transform="translate(12.9597 12.9597)" fill="#FAFAFA">
										</path>
										<path
											d="M0.196998 23.295L0.131434 23.4862L0.323216 23.4223L5.52771 21.6875C7.4273 22.8471 9.47325 23.4274 11.6637 23.4274C18.134 23.4274 23.4274 18.134 23.4274 11.6637C23.4274 5.19344 18.134 -0.1 11.6637 -0.1C5.19344 -0.1 -0.1 5.19344 -0.1 11.6637C-0.1 13.9996 0.624492 16.3352 1.93021 18.2398L0.196998 23.295ZM5.87658 19.8847L5.84025 19.8665L5.80154 19.8788L2.78138 20.8398L3.73978 17.9646L3.75932 17.906L3.71562 17.8623L3.43104 17.5777C2.27704 15.8437 1.55796 13.8245 1.55796 11.6637C1.55796 6.03288 6.03288 1.55796 11.6637 1.55796C17.2945 1.55796 21.7695 6.03288 21.7695 11.6637C21.7695 17.2945 17.2945 21.7695 11.6637 21.7695C9.64222 21.7695 7.76778 21.1921 6.18227 20.039L6.17557 20.0342L6.16817 20.0305L5.87658 19.8847Z"
											transform="translate(7.7758 7.77582)" fill="white" stroke="white"
											stroke-width="0.2">
										</path>
									</svg>
								</span>
							</span>
						</a>
					</div>
				</div>

				<div style="padding-top: 10px;">
					<Notice />
				</div>

			</div>
		</div>
	</div>
</template>

<script>
import Left from '../components/Left.vue';
import Right from '../components/Rightt.vue';
import Menu1 from '../components/contenttt.vue';
import Content from '@/components/Menuu.vue';
import Notice from '@/components/noticee.vue';

export default {
	name: 'Home',
	components: {
		Left,
		Right,
		Menu1,
		Content,
		Notice
	},
	data() {
		return {
			activeIndex: 0,
			menuItems: [
				{ name: 'Menu 1', activeSrc: '/menu-img/1-event-game.webp', inactiveSrc: '/menu-img/1-event-game.webp', component: 'Menu1', componentId: 'menu1' },
				{ name: 'Menu 2', activeSrc: '/menu-img/2-event-game.webp', inactiveSrc: '/menu-img/2-event-game.webp', component: 'Menu1', componentId: 'content' },
				{ name: 'Menu 3', activeSrc: '/menu-img/3-event-game.webp', inactiveSrc: '/menu-img/3-event-game.webp', component: 'Menu1', componentId: 'content' },
				{ name: 'Menu 4', activeSrc: '/menu-img/4-event-game.webp', inactiveSrc: '/menu-img/4-event-game.webp', component: 'Menu1', componentId: 'content' },
				{ name: 'Menu 5', activeSrc: '/menu-img/6-event-game.webp', inactiveSrc: '/menu-img/6-event-game.webp', component: 'Menu1', componentId: 'content' },

			],
		};
	},
	computed: {
		currentComponent() {
			return this.menuItems[this.activeIndex].component;
		}
	},
	methods: {
		setActive(index, componentId) {
			this.activeIndex = index;
			if (index === 0) {
				this.scrollTo(componentId);
			} else {
				this.scrollTo('content');
			}
		},
		scrollTo(id) {
			const element = document.getElementById(id);
			if (element) {
				element.scrollIntoView({ behavior: 'smooth' });
			}
		},
	},
};
</script>

<style scoped>
.icon_col {
	display: grid;
	gap: 0.5rem;
	position: fixed;
	bottom: 230px;
	left: 30px;
}

.icon {
	display: grid;
	position: absolute;
	gap: 0.5rem;
	right: 63px;
}

.bg {
	background-image: url('/public/image/bg.webp');
	background-size: cover;

}

.left {
	height: 100%;
}

.right {
	height: 100%;
}

.leftright_bg {
	background: rgba(0, 0, 0, .3);
	height: 100%;
	border-right: 1px solid rgba(255, 255, 255, .5);
}

.right_bg {
	background: rgba(0, 0, 0, .3);
	height: 100%;
	border-left: 1px solid rgba(255, 255, 255, .5);
}

.nav-link.active {
	border-bottom: 5px solid white;
}

.nav-link {
	border-bottom: 1px solid white;
}


@media (max-width: 768px) {

	.leftright_bg {
		background: rgba(0, 0, 0, 0);
		height: 100%;
		border-right: 0px solid rgba(255, 255, 255, .5);
	}

	.right_bg {
		background: rgba(0, 0, 0, 0);
		height: 100%;
		border-left: 0px solid rgba(255, 255, 255, .5);
	}

	.nav-pills {
		display: flex;
		overflow-x: auto;
		white-space: nowrap;
		padding: 0;
	}

	.nav-link {
		flex: 0 0 auto;
		width: 20%;
		text-align: center;
		padding: 0;
	}

	.left {
		padding-bottom: 0px;
	}

	.nav-link img {
		width: 100% !important;
	}
}

.nav-link img {
	width: 70%;
}


.nav-item {
	font-weight: bolder;
}

.nav-pills {
	--bs-nav-pills-link-active-bg: none;
	display: flex;
	flex-wrap: nowrap;
	padding: 10px 10px 10px 10px;
}

.menu_col {
	padding-bottom: 10px;
}



.main-col img {
	width: 90%;
}

@media screen and (max-width:768px) {
	.main-col {
		grid-template-columns: repeat(3, 1fr);
	}


}

@media screen and (max-width:767px) {
	.mobile_col {
		order: 2;
	}

	.mobile_col2 {
		order: 3;
	}
}

.content {
	padding-left: 12px;
	padding-right: 12px;
}

h1 {
	font-size: 25px;
	font-weight: bolder;
}

h2 {
	font-size: 23px;
	font-weight: bolder;
}

h3 {
	font-size: 15px;
	font-weight: bolder;
}


.nav-pills {
	display: flex;
	flex-wrap: nowrap;
	padding: 0;
	overflow-x: auto;
	/* 启用水平滚动 */
	white-space: nowrap;
	/* 防止换行 */
}

.nav-link {
	flex: 1;
	/* 使菜单项均匀分布 */
	text-align: center;
	padding: 0;
}

@media (max-width: 768px) {
	.nav-pills {
		flex-direction: row;
		/* 确保菜单项在水平行中 */
	}

	.nav-link {
		flex: 1;
		width: 20%;
	}

	.center_col {
		padding-top: 20px !important;
	}
}
</style>
