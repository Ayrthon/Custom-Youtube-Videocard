// INRELEASE CUSTOM YOUTUBE PLAYER
console.log (`
████████╗██╗  ██╗ ██████╗ ███╗   ██╗██╗██╗  ██╗████████╗██╗   ██╗
╚══██╔══╝██║  ██║██╔═══██╗████╗  ██║██║██║ ██╔╝╚══██╔══╝██║   ██║
   ██║   ███████║██║   ██║██╔██╗ ██║██║█████╔╝    ██║   ██║   ██║
   ██║   ██╔══██║██║   ██║██║╚██╗██║██║██╔═██╗    ██║   ╚██╗ ██╔╝
   ██║   ██║  ██║╚██████╔╝██║ ╚████║██║██║  ██╗██╗██║    ╚████╔╝ 
   ╚═╝   ╚═╝  ╚═╝ ╚═════╝ ╚═╝  ╚═══╝╚═╝╚═╝  ╚═╝╚═╝╚═╝     ╚═══╝  
   ------------------ CUSTOM YOUTUBE PLAYER -------------------
                  v1.1  Created by Thonik.tv ©
`);

// For a working demo: INRELEASE.NL

// YOUTUBE IFRAME API

// global variable for the player
var player;

// this function gets called when API is ready to use
function onYouTubePlayerAPIReady() {
  // create the global player from the specific iframe (#video)
  player = new YT.Player("video", {
    playerVars: {
      rel: 0,
    },
    events: {
      // call this function when player is ready to use
      onReady: onPlayerReady,
      onStateChange: onPlayerStateChange,
    }
  });
}

// Hide div when video is pause
function onPlayerStateChange(event) {
  if (event.data == YT.PlayerState.PAUSED) {
    hideVideo(); // this function is written below
  }
}

function onPlayerReady(event) {
  // bind events
  var playButton = document.getElementById("play-button");
  playButton.addEventListener("click", function () {
    player.playVideo();
    player.unMute(); //unMute when video is muted
    player.setVolume(100); // 0 - 100
  });

  var pauseButton = document.getElementById("pause-button");
  pauseButton.addEventListener("click", function () {
    player.pauseVideo();
  });
}

// Inject YouTube API script
var tag = document.createElement("script");
tag.src = "//www.youtube.com/player_api";
var firstScriptTag = document.getElementsByTagName("script")[0];
firstScriptTag.parentNode.insertBefore(tag, firstScriptTag);


// show/hide youtube video div
function showVideo() {
    var divElement = document.querySelector(".youtube");
    if ((divElement.style.visibility !== "visible") || (divElement.style.opacity !== "1")) {
        divElement.style.visibility = "visible";
        divElement.style.opacity = "1";
      } else {
        divElement.style.visibility = "hidden";
        divElement.style.opacity = "0";
      }
}

function hideVideo() {
  var divElement = document.querySelector(".youtube");
  if ((divElement.style.visibility !== "hidden" ) || (divElement.style.opacity !== "0")) {
      divElement.style.visibility = "hidden";
      divElement.style.opacity = "0";
    } else {
      divElement.style.visibility = "visible";
      divElement.style.opacity = "1";
    }
}

