<script>
    export let dialogID = 0;

    let dialogs;
    async function loadDialogs() {
        const response = await fetch("../narration/dialogs.json");
        dialogs = await response.json();
    }

    let imgData = "";
    let imgSrc = "";

    async function loadImg(scenename) {
        const img = await import(`./scenes/${scenename}`);
        imgData = img.default;
    }

    function handleImgLoad() {
        if (/\.gif$/i.test(imgSrc)) {
            imgSrc = imgSrc.replace(/\.gif$/, ".gif?rnd=" + Math.floor(Math.random() * 100) + 1);
        }
    }

    $: loadDialogs();
    $: loadImg(dialogs[dialogID].scenename);
</script>

<img src={imgSrc} on:load={handleImgLoad} alt="Error while loading scene" class="Scene" />

<style>
img {
  position: absolute;
  display: block;
  height: 100%;
  width: 100%;
}   

</style>