<html>
    <head>
        <style>
            body, html {
                margin: 0;
                padding: 0;
                width: 100%;
                height: 100%;
                background: #000;
            }
            #container {
                width: 100%;
                height: 100%;
                position: relative;
            }
            #fullscreen-btn {
                position: absolute;
                top: 10px;
                right: 10px;
                z-index: 99;
                padding: 10px 20px;
                background: #0064ff;
                color: white;
                border: none;
                cursor: pointer;
                border-radius: 5px;
                font-family: Arial, sans-serif;
            }
        </style>
    </head>
    <body>
        <div id="container">
            <button id="fullscreen-btn" onclick="goFullscreen()">Go Fullscreen</button>
            <div id="game" style="width:100%;height:100%;"></div>
        </div>

        <script>
            EJS_player = "#game";
            EJS_core = "nes";
            EJS_gameName = "Michael Jackson Bros.";
            EJS_color = "#0064ff";
            EJS_startOnLoaded = true;
            EJS_pathtodata = "https://cdn.emulatorjs.org/stable/data/";
            EJS_gameUrl = "Super Mario Bros. (World).nes";

            function goFullscreen() {
                const elem = document.getElementById("container");
                if (elem.requestFullscreen) {
                    elem.requestFullscreen();
                } else if (elem.webkitRequestFullscreen) { /* Safari */
                    elem.webkitRequestFullscreen();
                } else if (elem.msRequestFullscreen) { /* IE11 */
                    elem.msRequestFullscreen();
                }
            }

            // Listen for fullscreen change to hide/show button
            document.addEventListener('fullscreenchange', () => {
                const btn = document.getElementById('fullscreen-btn');
                if (document.fullscreenElement) {
                    btn.style.display = 'none';
                } else {
                    btn.style.display = 'block';
                }
            });
        </script>
        <script src="https://cdn.emulatorjs.org/stable/data/loader.js"></script>
    </body>
</html>
