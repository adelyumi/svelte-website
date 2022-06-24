<script lang="ts">
	import { Router, Route, Link } from "svelte-navigator";
	import AboutMe from "./AboutMe.svelte";
	import MyProjects from "./MyProjects.svelte";
	import RandomDog from "./RandomDog.svelte";
</script>

<Router>
	<header class="header">
		<nav>
			<Link to="about">About Me</Link>
			<Link to="projects">My Projects</Link>
			<Link to="api">Random Dog</Link>
		</nav>
	</header>

	<Route path="about/*aboutRoute" component={AboutMe} />

	<Route path="projects/*myProjects" component={MyProjects} />

	<Route path="api/*RandomDog" component={RandomDog} />

	<Route path="">
		<main>
			<h1>Adelina Kildeeva</h1>
			<img
				id="frog1"
				src="https://thumbs.gfycat.com/BetterPlumpAstrangiacoral-max-1mb.gif"
				alt="frog gif"
			/>
			<div id="block1">
				<p>Welcome to my website!</p>
				<p>I am a future IT-specialist and like to learn new things.</p>
			</div>
		</main>
	</Route>
	<footer>
		<a href="https://vk.com/adelina_yumi"
			><img
				class="logo"
				src="https://i.ibb.co/cQL9m6T/vk-48.png"
				alt="vk logo"
			/></a
		>
		<a href="https://t.me/yumiue"
			><img
				class="logo"
				src="https://i.ibb.co/VtrBKbY/telegram-48.png"
				alt="tg logo"
			/></a
		>
		<a href="https://github.com/adelyumi"
			><img
				class="logo"
				src="https://i.ibb.co/KLk2zQc/github-11-48.png"
				alt="github logo"
			/></a
		>
		<p id="email">email: a.kildeeva@innopolis.university</p>
	</footer>
</Router>

<style>
	.header {
		padding: 0.5em;
		padding-left: 3em;
		text-align: left;
		background-color: #a4c2a5;
	}

	h1 {
		margin-top: 0.9em;
		margin-bottom: 0;
		font-size: 90px;
		color: #a4c2a5;
	}

	p {
		color: #566246;
	}

	#frog1 {
		width: 8.5em;
	}

	#block1 {
		margin-top: 1em;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 2em;
		background-color: #f1f2eb;
		padding: 5px;
		width: 30%;
	}

	footer {
		padding-top: 0.6em;
		background-color: #a4c2a5;
		position: absolute;
		bottom: 0;
		width: 99%;
	}

	.logo {
		width: 1.5em;
		margin-right: 0.8em;
		margin-bottom: 0em;
	}

	.logo:hover {
		opacity: 0.3;
	}

	#email {
		margin-top: 0.5%;
		color: #ffffff;
	}

</style>
