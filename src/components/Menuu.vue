<template>
	<h1 style="color: white; padding-top: 10px;">{{ $t('MB8.title') }}</h1>
	<p>
		{{ $t('MB8.1') }}
		<b>{{ $t('MB8.2') }}</b>
		{{ $t('MB8.3') }}
		<b>{{ $t('MB8.4') }}</b>
		{{ $t('MB8.5') }}
	</p>
	<br>
	<p>
		{{ $t('MB8.6') }}
		<b>{{ $t('MB8.7') }}</b>
		{{ $t('MB8.8') }}
	</p>
	<br>
	<br>

	<h3 style="color: white;">
		{{ $t('memberToday.title') }}
	</h3>
	<p>
		{{ $t('memberToday.1') }}
		<b>
			{{ $t('memberToday.2') }}
		</b>
		{{ $t('memberToday.3') }}
	</p>
	<br>
	<ol style="color: white;">
		<li>
			{{ $t('memberToday.4') }}
			<b>{{ $t('memberToday.5') }}</b>
			{{ $t('memberToday.6') }}
		</li>
		<li>
			{{ $t('memberToday.7') }}
		</li>
		<li>
			{{ $t('memberToday.8') }}
			<b>{{ $t('memberToday.9') }}</b>
			{{ $t('memberToday.10') }}
		</li>
		<li>
			{{ $t('memberToday.11') }}
		</li>
		<li>
			{{ $t('memberToday.12') }}
			<b>
				{{ $t('memberToday.13') }}
			</b>
			{{ $t('memberToday.14') }}
		</li>
		<li>
			{{ $t('memberToday.15') }}
			<b>{{ $t('memberToday.16') }}</b>
			{{ $t('memberToday.17') }}
		</li>
	</ol>
	<br>
	<p>
		{{ $t('memberToday.18') }}
		<b>{{ $t('memberToday.19') }}</b>
		{{ $t('memberToday.20') }}
	</p>

	<br>
	<br>

	<h3 style="color: white;">
		{{ $t('payandplay.title') }}
	</h3>
	<p>
		{{ $t('payandplay.1') }}
		<b>
			{{ $t('payandplay.2') }}
		</b>
		{{ $t('payandplay.3') }}
	</p>

	<br><br>
	<h3 style="color: white;">
		{{ $t('BestSlotProviders.title') }}
	</h3>
	<p>
		{{ $t('BestSlotProviders.1') }}
	</p>
	<ul style="color: white;">
		<li>
			<b>
				{{ $t('BestSlotProviders.2') }}
			</b>
			{{ $t('BestSlotProviders.3') }}
			{{ $t('BestSlotProviders.4') }}
		</li>
		<li>
			<b>
				{{ $t('BestSlotProviders.5') }}
			</b>
			{{ $t('BestSlotProviders.6') }}
		</li>
		<li>
			<b>
				{{ $t('BestSlotProviders.7') }}
			</b>
			{{ $t('BestSlotProviders.8') }}
		</li>
	</ul>
	<br>
	<p>
		{{ $t('BestSlotProviders.9') }}
		<b>
			{{ $t('BestSlotProviders.10') }}
		</b>
		{{ $t('BestSlotProviders.11') }}
	</p>

	<br>
	<a href="//www.dmca.com/Protection/Status.aspx?ID=bd071465-17bf-4b90-b6e5-d51ffeb2271e" rel="nofollow"
		title="DMCA.com Protection Status" class="dmca-badge"> <img
			src="https://images.dmca.com/Badges/dmca_copyright_protected150c.png?ID=bd071465-17bf-4b90-b6e5-d51ffeb2271e"
			alt="DMCA.com Protection Status" /></a>

	<br><br>
	<p style="font-weight: 700; color: #fff;">
		{{ $t('Footer.title') }}
	</p>

	<p style="color: #fff;">
		<a :href="link2" style="font-weight: 900; color:#FFD700;">
			{{ $t('Footer.1') }}</a>
		| {{ $t('Footer.2') }}
	</p>

	<p style="color: #fff;">
		<a :href="link" style="font-weight: 900;color:#FFD700; ">
			{{ $t('Footer.3') }}</a>
		| {{ $t('Footer.4') }}
	</p>
	<p>
		<b>
			{{ $t('Footer.5') }}
		</b>
	</p>
	<p style="padding-bottom: 50px;">
		{{ $t('Footer.6') }}
	</p>


	<div class="col-12">
		<div class="row">
			<div class="gamelicense-content">
				<h3 style="color: white;">{{ $t('gamelicense.1') }}</h3>
				<div class="game-license">
					<div class="gc-logo">
						<img src="/public/image/gc.webp" alt="gc-logo">

					</div>
					<div class="gc-content">
						<p class="gctext" style="color: white;">
							{{ $t('GCcontent.gc') }}
						</p>
					</div>
				</div>
				<h3 style="color: white;">{{ $t('gamelicense.2') }}</h3>
				<div style="padding-bottom: 20px; justify-content: center;" class="col-12">

					<img width="70%" src="/public/image/bank-logo.webp" alt="bank-logo">
				</div>
				<h3 style="color: white;">{{ $t('gamelicense.3') }}</h3>
				<div style="padding-bottom: 20px; justify-content: center;" class="col-12">

					<img width="70%" src="/public/image/bmm-logo.webp" alt="bmm-logo">
				</div>

			</div>
			<div class="footer">
				<p>Copyright © MB8. All rights reserved.</p>
			</div>
		</div>

	</div>



</template>
<script>
import axios from 'axios';
export default {
	name: 'Content',
	data() {
		return {
			link: "",
			link2: ""
		}
	},
	methods: {
		async calllink() {
			try {
				const response = await axios.get('https://seo.mobileapplab.online/api/atas?fields[0]=ataskasino_com', {
					headers: {
						"Authorization": "Bearer " + "1c4db3188ab2e9a077928920d9cc8d3322d15f9751bc2054a5cb70008df79cf3e3a4dd005a75a1f2db40eb953292ee10ef699693e96e9d77a98439f438ee6a6e6805a8a955e992f082b9e6118a4345e1ed18438ff9789edf9ed1dd58af45ee6669a7519a1291746959ff45bc2054b7f408b5da5ea8cd04d588a2704b7e218021",
					}
				});
				this.link = response.data.data.attributes.ataskasino_com;

				console.log(this.link);
			} catch (error) {
				console.error(error);
			}
		},
		async calllink2() {
			try {
				const response = await axios.get('https://seo.mobileapplab.online/api/atas?fields[0]=atascasinobet_com', {
					headers: {
						"Authorization": "Bearer " + "1c4db3188ab2e9a077928920d9cc8d3322d15f9751bc2054a5cb70008df79cf3e3a4dd005a75a1f2db40eb953292ee10ef699693e96e9d77a98439f438ee6a6e6805a8a955e992f082b9e6118a4345e1ed18438ff9789edf9ed1dd58af45ee6669a7519a1291746959ff45bc2054b7f408b5da5ea8cd04d588a2704b7e218021",
					}
				});
				this.link2 = response.data.data.attributes.atascasinobet_com;

				console.log(this.link2);
			} catch (error) {
				console.error(error);
			}
		},
	},
	mounted() {
		this.calllink();
		this.calllink2();
	}
}
</script>
<style>
h1 {
	color: white;
	font-size: 25px !important;
	font-weight: bolder !important;
}

h2 {
	color: white;
	font-size: 23px !important;
	font-weight: bolder !important;
}

h3 {
	color: white;
	font-size: 18px !important;
	font-weight: bolder !important;
}

p {
	color: white;
}

.gc-logo img {
	width: 70% !important;
}

@media screen and (max-width:768px) {
	.gc-logo img {
		width: 100% !important;
	}
}

.gamelicense-content h3 {
	font-size: 12px !important;
}

.game-license {
	display: flex;
	gap: 1rem;
	padding: 10px;
	padding-bottom: 20px;
	justify-content: center;
}

.gc-logo {
	width: 30%;
	flex: 0 0 auto;
}

.gc-content {
	width: 65%;
	flex: 0 0 auto;
	font-size: 12px
}

.gctext {
	color: white;
	font-size: 12px;
}


@media screen and (max-width:546px) {
	.gctext {
		font-size: 8px !important;
	}
}

.footer {
	color: white;
	text-align: center;
	font-size: 12px;
}
</style>
