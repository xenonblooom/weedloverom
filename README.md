<!DOCTYPE html>
<html>
<head>
    <title>List of Songs stolen from me </title>
    <link href="https://fonts.googleapis.com/css2?family=Permanent+Marker&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: Arial, sans-serif;
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            grid-template-rows: repeat(2, 1fr);
            height: 100vh;
            margin: 0;
        }

        body div {
            background-size: cover;
            background-position: center;
            filter: brightness(60%);
            border: 1px solid rgba(255,255,255,0.1);
        }

        .bg1 {
            background-image: url('https://static.stereogum.com/uploads/2015/08/2Pac-and-Snoop-Dogg-640x445.jpg');
            grid-column: 1 / 3;
            grid-row: 1;
        }

        .bg2 {
            background-image: url('https://i.ytimg.com/vi/cCs5VnZ5FZI/maxresdefault.jpg');
            grid-column: 1;
            grid-row: 2;
        }

        .bg3 {
            background-image: url('http://www.dommune.com/ele-king/upload/img/733.jpg');
            grid-column: 2;
            grid-row: 2;
        }

        .title {
            font-family: 'Permanent Marker', cursive;
            font-size: 3em;
            text-align: center;
            padding-top: 20px;
            color: #ff0;
            grid-column: 1 / 3;
            grid-row: 1 / 3;
            z-index: 1;
        }

        .list {
            font-family: 'Permanent Marker', cursive;
            font-size: 1.5em;
            text-align: center;
            color: #ddd;
            list-style-type: none;
            padding: 20px 0;
            grid-column: 1 / 3;
            grid-row: 1 / 3;
            z-index: 1;
        }

        .list li {
            margin: 10px 0;
        }

        .list a {
            color: #0f0;
        }
    </style>
</head>
<body>
    <div class="title">List of Songs stolen from me </div>
    <div class="bg1"></div>
    <div class="bg2"></div>
    <div class="bg3"></div>
    <ul class="list" id="songs-list">
        <!-- Songs will be dynamically added here with JavaScript -->
    </ul>

    <script>
        // Define your list of songs and their links
        var songs = [
            {name: "OM's plan", link: "https://youtu.be/xpVfcZ0ZcFM?si=Bin4e6iDPVvpQjom"},
            {name: "freestyle vol.1", link: "https://youtu.be/XbGs_qK2PQA?si=v36LNreV3EatV5Q1"},
            {name: "yesterday's spagetti", link: "https://www.youtube.com/watch?v=xFYQQPAOz7Y&ab_channel=EminemMusic"},
            {name: "convo with my niece", link: "https://www.youtube.com/watch?v=SRcnnId15BA&ab_channel=50CentVEVO"},
            {name: "this episode", link: "https://www.youtube.com/watch?v=QZXc39hT8t4&ab_channel=DrDreVEVO"},
            // Add more songs here...
        ];

        // Get the songs list element
        var songsListElement = document.getElementById("songs-list");

        // Add each song to the list
        for (var i = 0; i < songs.length; i++) {
            var song = songs[i];
            var songElement = document.createElement("li");
            songElement.innerHTML = '<a href="' + song.link + '">' + song.name + '</a>';
            songsListElement.appendChild(songElement);
        }
    </script>
</body>
</html>
