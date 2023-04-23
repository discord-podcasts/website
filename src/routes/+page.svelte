<script>
	import Nav from '../components/Nav.svelte';
	import Fa from 'svelte-fa/src/fa.svelte'
	import {faChevronDown} from '@fortawesome/free-solid-svg-icons'
	import {faJava, faPython, faRust, faSquareJs} from '@fortawesome/free-brands-svg-icons'
	import FeaturedBot from './FeaturedBot.svelte';
</script>

<div class="wrapper">
	<Nav/>
	<div class="container">
		<div>
			<h1>Discord Podcasts</h1>
		</div>
		<div>
			<h2>Connect Servers</h2>
			<h2>Connect People</h2>
			<h2>Connect Bots</h2>
		</div>
		<div class="buttons">
			<a class="button-1 what-button" href="#about">
				What?
				<Fa icon={faChevronDown}/>
			</a>
		</div>
	</div>
	<div class="transition"></div>
</div>
<div class="content-wrapper" id="about">
	<div class="content-container about-container">
		<h2>What is Discord Podcasts?</h2>
		<p>Discord Podcasts is an API which makes it possible to have cross server stages! It allows bots to share their audio data and stream it to different
		   clients. You can imagine it something like a radio. Multiple clients are able to stream the audio from the server in realtime. With this you are able to
		   listen to stage channels in your own server. This makes discovery a lot easier.</p>
	</div>
</div>
<div class="content-wrapper">
	<div class="content-container">
		<h2>Start listening to podcasts!</h2>
		<p>Start using Discord Podcasts by inviting one of our partnered bots</p>
		<div class="bots">
			<FeaturedBot icon="https://myra.bot/logo.png" name="Myra"/>
			<FeaturedBot icon="https://avatars.githubusercontent.com/u/107505069?s=200&v=4" name="Discord Podcasts"/>
		</div>
	</div>
</div>
<div class="content-wrapper">
	<div class="content-container">
		<h2>Our API wrappers</h2>
		<div class="wrappers">
			<div class="api-wrapper">
				<Fa icon={faJava} style="color: white; font-weight: bold; font-size: 5rem"/>
			</div>
			<div class="api-wrapper">
				<Fa icon={faSquareJs} style="color: white; font-weight: bold; font-size: 5rem"/>
			</div>
			<div class="api-wrapper">
				<Fa icon={faPython} style="color: white; font-weight: bold; font-size: 5rem"/>
			</div>
			<div class="api-wrapper">
				<Fa icon={faRust} style="color: white; font-weight: bold; font-size: 5rem"/>
			</div>
		</div>
	</div>
</div>

<style>
	.wrapper {
		width: 100vw;
		height: 100vh;

		display: flex;
		align-items: center;
		justify-content: center;

		background-image: url("discord-podcasts-background.png");
		background-size: cover;
	}

	.container {
		display: flex;
		flex-direction: column;
		justify-content: center;
		gap: 1.5rem;
	}
	.buttons { display: flex; }
	.what-button { font-size: 1.5rem }
	.transition {
		position: absolute;
		width: 100%;
		height: 100px;
		bottom: 0;
		background: linear-gradient(0deg, var(--primary-050) 0%, transparent 100%);
	}

	.content-wrapper {
		display: flex;
		align-items: center;
		justify-content: center;
		margin-top: 5rem;
	}
	.content-container {
		width: 60%;
		display: flex;
		flex-direction: column;
		gap: 1rem;
	}

	/* About */
	.about-container p {
		font-size: 1.2rem;
		line-height: 1.2;
		max-width: 100ch;
	}

	/* Api wrappers */
	.wrappers {
		display: flex;
		flex-wrap: wrap;
		gap: 5rem;
	}
	.api-wrapper {
		width: 150px;
		height: 150px;

		display: flex;
		align-items: center;
		justify-content: center;

		border-radius: 20px;
		background-color: var(--primary-100)
	}

	.bots {
		display: flex;
		gap: 2.5rem;
	}
</style>