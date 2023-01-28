<script>
	import { dialogs } from '../narration/dialogs.json';
	/**
	 * @type {number}
	 */
	export let dialogID;
</script>

<div class="bubble">
	<div class="name">
		<p>{dialogs[dialogID].name}</p>
	</div>
	<p>{dialogs[dialogID].text}</p>
</div>

<style>
	.bubble {
		position: absolute;
		bottom: 0;
		left: 0;
		right: 0;
		width: 100%;
		padding: 20px;
		background-color: white;
		border-radius: 10px 10px 0 0;
		box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.3);
		font-size: 1.1rem;
	}

	.name {
		position: absolute;
		bottom: 100%;
		left: 5%;
		right: 0;
		width: 15%;
		text-align: center;
		height: 10%;
		padding: 20px;
		background-color: rgb(226, 146, 146);
		border-radius: 10px 10px 0 0;
		box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.3);
		font-size: 1.1rem;
	}

	.name p {
		transform: translateY(-50%);
	}
</style>
