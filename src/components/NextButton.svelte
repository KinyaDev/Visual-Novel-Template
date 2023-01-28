<script>
	import { dialogs } from '../dialogs.json';
	$: dialogID = 0;

	/**
	 * @type {(dialogID:number) => void}
	 */
	export let handleDialog;

	function handleNext() {
		if (dialogID === dialogs.length - 1) {
			console.log('end');
		} else {
			dialogID++;
			handleDialog(dialogID);
		}
	}
</script>

<button on:click={handleNext}>＞</button>

<style>
	button {
		cursor: pointer;
		position: absolute;
		background-color: transparent;
		height: 50px;
		width: 200px;
		font-size: 1.5em;
		border: transparent;
		color: rgb(226, 146, 146);
		bottom: 3.4%;
		left: 800x;
		right: 0;
	}
</style>
