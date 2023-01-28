<script>
	/**
	 * @type {number}
	 */
	export let dialogID;

	import { dialogs } from '../narration/dialogs.json';
</script>

<img
	src={`../scenes/${dialogs[dialogID].scenename}`}
	alt="Error while loading scene"
	class="Scene"
/>

<style>
	img {
		position: absolute;
		display: block;
		height: 100%;
		width: 100%;
	}
</style>
