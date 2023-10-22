## 2023 Primary Program Playlist

### Play audio in browser

<style>
    #playlist{
        list-style: none;
    }
    #playlist li a{
        color:black;
        text-decoration: none;
    }
    #playlist .current-song a{
        color:blue;
    }
</style>

<audio src="" controls id="audioPlayer">
    Sorry, your browser doesn't support HTML 5!
</audio>


<ul id="playlist">

<li class="current-song"><a href="https://github.com/drhyrum/2023-primary-program/raw/gh-pages/list/1-JesusOnceWasALittleChild.mp3">Jesus Once Was a Little Child</a></li>

<li><a href="https://github.com/drhyrum/2023-primary-program/raw/gh-pages/list/2-TellMeTheStoriesOfJesus.mp3">Tell Me the Stories of Jesus</a></li>
    
<li><a href="https://github.com/drhyrum/2023-primary-program/raw/gh-pages/list/3-KeepTheCommandments.mp3
">Keep the Commandments</a></li>

<li><a href="https://github.com/drhyrum/2023-primary-program/raw/gh-pages/list/4-IWillWalkWithJesus.mp3">I Will Walk With Jesus</a></li>

<li><a href="https://github.com/drhyrum/2023-primary-program/raw/gh-pages/list/5-IFeelMySaviorsLove.mp3">I Feel My Saviors Love</a></li>

<li><a href="https://github.com/drhyrum/2023-primary-program/raw/gh-pages/list/6-TeachMeToWalkInTheLight.mp3
">Teach Me to Walk in the Light</a></li>

<li><a href="https://github.com/drhyrum/2023-primary-program/raw/gh-pages/list/7-Gethsemane.mp3">Gethsemane</a></li>

<li><a href="https://github.com/drhyrum/2023-primary-program/raw/gh-pages/list/8-WhenHeComesAgain.mp3">When He Comes Again</a></li>

<li><a href="https://github.com/drhyrum/2023-primary-program/raw/gh-pages/list/9-HeSentHisSon.mp3">He Sent His Son</a></li>

<li><a href="https://github.com/drhyrum/2023-primary-program/raw/gh-pages/list/10-ImTryingToBeLikeJesus.mp3">I'm Trying To Be Like Jesus</a></li>  

<li><a href="https://github.com/drhyrum/2023-primary-program/raw/gh-pages/list/WhenJesusChristWasBaptized-CTR7-ONLY.mp3">(CTR 7 Only) When Jesus Christ Was Baptized</a></li>  
</ul>
    
<script src="https://code.jquery.com/jquery-2.2.0.js"></script>
<script>
    // loads the audio player
    audioPlayer();

       function audioPlayer(){
            var currentSong = 0;
            $("#audioPlayer")[0].src = $("#playlist li a")[0];
            $("#audioPlayer")[0].play();
            $("#playlist li a").click(function(e){
               e.preventDefault(); 
               $("#audioPlayer")[0].src = this;
               $("#audioPlayer")[0].play();
               $("#playlist li").removeClass("current-song");
                currentSong = $(this).parent().index();
                $(this).parent().addClass("current-song");
            });
            
            $("#audioPlayer")[0].addEventListener("ended", function(){
               currentSong++;
                if(currentSong == $("#playlist li a").length)
                    currentSong = 0;
                $("#playlist li").removeClass("current-song");
                $("#playlist li:eq("+currentSong+")").addClass("current-song");
                $("#audioPlayer")[0].src = $("#playlist li a")[currentSong].href;
                $("#audioPlayer")[0].play();
            });
        }    
</script>


<!-- ### Download a playlist

<a href="2022-primary-program-playlist.m3u" target="_blank" download type="audio/x-mpegurl">Download the playlist.</a> -->

<!-- ### QR Code to website

<img src="https://github.com/drhyrum/2022-primary-program/raw/gh-pages/primary_program_qr_code.png"> -->


