<script>
	import Counter from './Counter.svelte';
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcome_fallback from '$lib/images/svelte-welcome.png';
	import ChevronCircleUp from 'svelte-icons/fa/FaChevronCircleUp.svelte';
	import { AirplayIcon} from 'svelte-feather-icons';
	import github from '$lib/images/github.svg';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>


<section>
	<h1>
		<span class="welcome">
			<picture>
				<source srcset={welcome} type="image/webp" />
				<img src={welcome_fallback} alt="Welcome" />
			</picture>
		</span>

		to your new<br />SvelteKit app
	</h1>

	<h2>
		try editing <strong>src/routes/+page.svelte</strong>
	</h2>

	<Counter />
	<p> Svelte Icons </p>
	<div class="icon">
		<ChevronCircleUp />
	</div>	
	<p> Svelte Feather Icons </p>
	<AirplayIcon size="24" />

	<p> SVG icon</p>
	<img src={github} alt="GitHub" />


</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	h1 {
		width: 100%;
	}

	.welcome {
		display: block;
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}

	.welcome img {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		display: block;
	}

	.icon {
	  color: red;
	  width: 32px;
	  height: 32px;
	}

	svg {
		width: 2em;
		height: 3em;
		display: block;
	}
</style>
