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

<div>
	<Scene {dialogID} />
	<Dialog {dialogID} />
	<NextButton {handleDialog} />
</div>
