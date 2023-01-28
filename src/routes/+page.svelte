<script>
	import Scene from '../components/Scene.svelte';
	import Dialog from '../components/Dialog.svelte';
	import NextButton from '../components/NextButton.svelte';

	$: dialogID = 0;

	/**
	 *
	 * @param {number} dialogIDx
	 */

	let handleDialog = (dialogIDx) => {
		dialogID = dialogIDx;
	};
</script>

<svelte:head>
	<title>Visual Novel - Basic</title>
</svelte:head>

<div>
	<Scene {dialogID} />
	<div class="welcome">
		<h1>Welcome to the Template</h1>
		<h3>
			You should start by editing <code>src/dialogs.json</code> and adding your images in
			<code>static/scenes</code>
		</h3>
	</div>

	<Dialog {dialogID} />
	<NextButton {handleDialog} />
</div>

<style>
	.welcome {
		position: absolute;
		left: 5%;
		top: 5%;
	}

	.welcome h3 {
		font-size: 0.85rem;
		font-style: italic;
		margin-left: 3%;
	}
</style>
