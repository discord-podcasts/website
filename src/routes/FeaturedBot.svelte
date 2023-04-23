<script lang="ts">
	import Fa from 'svelte-fa/src/fa.svelte'
	import {faUpRightFromSquare} from '@fortawesome/free-solid-svg-icons'

	export let name: string
	export let icon: string
</script>

<div class="featured-bot">
	<img alt={name} src={icon}>
	<h3>{name}</h3>
	<a>
		Try now!
		<Fa icon={faUpRightFromSquare} style="font-size: .6rem"/>
	</a>
</div>

<style>
	.featured-bot {
		width: 200px;
		height: 200px;

		display: flex;
		align-items: center;
		justify-content: center;
		flex-direction: column;


		background-color: var(--primary-100);
		border-radius: 25px;
	}
	img {
		width: 40%;
		border-radius: 50%;
	}
	h3 {
		margin-top: 1rem;
		text-align: center;
	}
	a {
		cursor: pointer;
		font-size: .8rem;
		margin-top: .2rem;
		color: #4287F5;
	}
	a:hover { text-decoration: underline }
</style>