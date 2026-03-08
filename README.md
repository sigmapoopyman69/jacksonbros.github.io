    #game-container {
        width: 100vw;
        height: 100vh;
        display: flex;
        flex-direction: column;
    }

    #game {
        flex-grow: 1;
        width: 100%;
        height: 100%;
    }

    /* The Button */
    #fs-button {
        position: absolute;
        bottom: 20px;
        right: 20px;
        padding: 12px 20px;
        background: #0064ff;
        color: white;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        z-index: 9999;
        font-weight: bold;
    }

    /* Hides the button COMPLETELY whenever the container is in fullscreen */
    #game-container:fullscreen #fs-button {
        display: none !important;
    }
    #game-container:-webkit-full-screen #fs-button { /* Safari support */
        display: none !important;
    }
</style>
<div id="game-container">
    <div id="game"></div>
    <button id="fs-button" onclick="toggleFullScreen()">Play Fullscreen</button>
</div>

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
