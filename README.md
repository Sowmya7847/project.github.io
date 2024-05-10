<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Countdown Timer</title>
<style>
    /* CSS styling for the countdown timer */
    body {
        font-family: Arial, sans-serif;
        background-color: #f4f4f4;
        text-align: center;
    }

    h1 {
        color: #333;
    }

    #countdown {
        font-size: 4em;
        color: #ff5733;
    }
</style>
</head>
<body>
<h1>Countdown Timer</h1>
<div id="countdown"></div>
<script>
function countdown(time_sec) {
    var timer = setInterval(function() {
        if (time_sec <= 0) {
            clearInterval(timer);
            document.getElementById("countdown").innerHTML = "stop";
        } else {
            var mins = Math.floor(time_sec / 60);
            var secs = time_sec % 60;
            var timeformat = (mins < 10 ? '0' : '') + mins + ':' + (secs < 10 ? '0' : '') + secs;
            document.getElementById("countdown").innerHTML = timeformat;
            time_sec--;
        }
    }, 1000);
}
// Start the countdown with 300 seconds (5 minutes)
countdown(300);
</script>
</body>
</html>
