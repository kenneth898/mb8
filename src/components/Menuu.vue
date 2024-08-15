<template>
	<a href="//www.dmca.com/Protection/Status.aspx?ID=bd071465-17bf-4b90-b6e5-d51ffeb2271e" rel="nofollow"
		title="DMCA.com Protection Status" class="dmca-badge"> <img
			src="https://images.dmca.com/Badges/dmca_copyright_protected150c.png?ID=bd071465-17bf-4b90-b6e5-d51ffeb2271e"
			alt="DMCA.com Protection Status" /></a>


	<!-- <p style="font-weight: 700; color: #fff;">
		{{ $t('Footer.title') }}
	</p>

	<p style="color: #fff;">
		<a style="font-weight: 900; color:#FFD700;" href="https://www.atascasinobet.com/">{{
			$t('Footer.1') }}</a>
		| {{ $t('Footer.2') }}|
		{{ $t('Footer.3') }}
	</p>

	<p style="padding-bottom: 80px; color: #fff;">
		<a style="font-weight: 900;color:#FFD700; " href="https://www.ataskasino.com/">{{ $t('Footer.4')
			}}</a>
		| {{ $t('Footer.5') }}
	</p> -->
	<br><br>
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
export default {
	name: 'Content'
}
</script>
<style>
h1 {
	font-size: 25px !important;
	font-weight: bolder !important;
}

h2 {
	font-size: 23px !important;
	font-weight: bolder !important;
}

h3 {
	font-size: 18px !important;
	font-weight: bolder !important;
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
