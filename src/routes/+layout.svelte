<script>
	import Header from './Header.svelte';
	import logo from '$lib/images/AchilleaStudios-Logo-RGB-A-Offset.png'
	import '../app.css';	
</script>

<div class="app">
	<Header />

	<main>
		<slot />
	</main>

	<footer>
		<div class="footerText"><a href="/">HOME</a> <a href="/about">ABOUT</a> <a href="/contact">CONTACT</a></div>
		<div><img src={logo} alt="the achillea studios logo, styalized red & yellow flowers next to a quilt square" /> </div>
		<div class="subText">Built with <a href="https://getloom.org" target="_blank">Loom</a></div>
		<div class="subText">Designed by <a href="https://www.ainsleestudios.com/" target="_blank">Ainslee Studios</a></div>
	</footer>
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 64rem;
		margin: 0 auto;
		box-sizing: border-box;
		font-family: Metropolis;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 12px;
        font-size: 2em;
		font-family: Metropolis;
		overflow: auto;
		
	}

	footer a {
		font-weight: bold;
        margin-left: 1%;
        margin-right: 1%;
        margin-bottom: 2%;
	}

	.footerText {
		display: flex;
		flex-direction: row;;
	}

	.subText {
		font-size: 0.4em;
		flex-shrink: 0;
		white-space: nowrap
	}

	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}

	img {
        height: 3em;
    }
</style>