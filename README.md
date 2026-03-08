
<script>
    EJS_player = "#game";
    EJS_core = "nes";
    EJS_gameName = "Michael Jackson Bros.";
    EJS_color = "#0064ff";
    EJS_startOnLoaded = true;
    EJS_pathtodata = "https://cdn.emulatorjs.org/stable/data/";
    EJS_gameUrl = "Super Mario Bros. (World).nes";

    function toggleFullScreen() {
        const elem = document.getElementById("game-container");
        if (!document.fullscreenElement) {
            if (elem.requestFullscreen) {
                elem.requestFullscreen();
            } else if (elem.webkitRequestFullscreen) {
                elem.webkitRequestFullscreen();
            }
        } else {
            if (document.exitFullscreen) {
                document.exitFullscreen();
            }
        }
    }
</script>
<script src="https://cdn.emulatorjs.org/stable/data/loader.js"></script>
