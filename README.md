<title>Michael Jackson Bros.</title> <style> body, html { margin: 0; padding: 0; height: 100%; width: 100%; overflow: hidden; background-color: #000; }
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

<html>
    <head>
        <!--HTML file auto generated using EmulatorJS codehelper-->
        <style>
            body, html {
                margin: 0;
                padding: 0;
            }
        </style>
    </head>
    <body>
        <div style="width:100%;height:100%;max-width:100%">
            <div id="game"></div>
        </div>
        <script>
            EJS_player = "#game";
            EJS_core = "nes";
            EJS_gameName = "Michael Jackson Bros.";
            EJS_color = "#0064ff";
            EJS_startOnLoaded = true;
            EJS_pathtodata = "https://cdn.emulatorjs.org/stable/data/";
            EJS_gameUrl = "Super Mario Bros. (World).nes";
        </script>
        <script src="https://cdn.emulatorjs.org/stable/data/loader.js"></script>
    </body>
</html>
