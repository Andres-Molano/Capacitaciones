<template>
  <div class="container">
      <div class="player">
        <div class="player__controls">
          <div class="player__btn player__btn--small" id="previous">
            <i class="fas fa-arrow-left"></i>
          </div>
          <h5 class="player__title">playing now</h5>
          <div class="player__btn player__btn--small" id="icon-menu">
            <i class="fas fa-bars"></i>
          </div>
        </div>
        <div class="player__album">
          <img
            src="https://i.ibb.co/ZS3wRSh/cover.jpg"
            alt="Album Cover"
            class="player__img"
            loading="lazy"
          />
        </div>

        <h2 class="player__artist">Disclosure</h2>
        <h3 class="player__song">Latch</h3>

        <input
          type="range"
          value="20"
          min="0"
          class="player__level"
          id="range"
        />
        <div class="audio-duration">
          <div class="start">00:01</div>
          <div class="end">04:30</div>
        </div>

        <audio ref="audio" class="player__audio" controls id="audio">
          <source
            src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/308622/Leo%20-%20Trying.mp3"
            type="audio/mpeg"
          />
        </audio>

        <div class="player__controls">
          <div class="player__btn player__btn--medium" id="backward">
            <i class="fas fa-backward"></i>
          </div>

          <div class="player__btn player__btn--medium blue play" @click="music()" id="play">
            <i ref="play" class="fas fa-play play-btn"></i>
            <i ref="pause" class="fas fa-pause pause-btn hide"></i>
          </div>

          <div class="player__btn player__btn--medium" id="forward">
            <i class="fas fa-forward"></i>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
export default {

  methods: {
    music(){
      if(this.$refs.audio.paused || this.$refs.audio.ended ){
        this.$refs.play.classList.toggle("hide");
        this.$refs.pause.classList.toggle("hide");
        this.$refs.audio.play()
      }else{
        this.$refs.audio.pause();
        this.$refs.play.classList.toggle("hide");
        this.$refs.pause.classList.toggle("hide");
      }
    }
  }
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Raleway:wght@400;500&display=swap");
@import "../assets/sass/vars.scss";

*,
*::before,
*::after {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: "Raleway", sans-serif;
}

img {
  max-width: 100%;
}

.container {
  background-color: $background;
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
}

.player {
  width: 300px;
  height: 550px;
  background-color: var(--background);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  border-radius: 12px;
  box-shadow: 9px 9px 16px rgba(163, 177, 198, 0.6),
    -9px -9px 16px rgba(255, 255, 255, 0.5);
}

.player__controls {
  display: flex;
  width: 95%;
  justify-content: space-evenly;
  align-items: center;
  margin-bottom: 25px;
}

.player__btn {
  cursor: pointer;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  box-shadow: -8px -8px 20px 0px #fff9, -6px -6px 6px 0px #fff9,
    8px 8px 20px #0001, 5px 5px 6px 0px #0001;
  color: var(--gray);
}

.player__btn:active {
  box-shadow: inset -8px -8px 20px #fff9, inset -5px -5px 6px #fff9,
    inset 8px 8px 20px #0003, inset 5px 5px 6px #0001;
}

.player__btn--small {
  min-width: 50px;
  min-height: 50px;
}

.player__title {
  font-weight: 600;
  font-size: 0.8em;
  color: #a1a1a1;
  text-transform: uppercase;
  letter-spacing: 2px;
  margin: 0;
}

.player__album {
  width: 150px;
}

.player__img {
  border-radius: 50%;
  box-shadow: 2px 2px 7px rgb(163, 177, 198), -2px -2px 7px rgb(163, 177, 198),
    -8px -8px 50px rgba(255, 255, 255, 0.8), 3px 3px 25px rgba(0, 0, 0, 0.6);
}

.player__artist {
  font-size: 1.2em;
  font-weight: 500;
  opacity: 0.5;
  margin: 20px 0px 0px 0px;
}

.player__song {
  position: relative;
  width: 100%;
  text-align: center;
  font-weight: 400;
  font-size: 1em;
  opacity: 0.5;
  margin: 0;
}

.player__level {
  width: 80%;
  -webkit-appearance: none;
  outline: none;
  border: none;
  padding: 0;
  margin-top: 40px;
}

.player__level::-webkit-slider-runnable-track {
  background-color: #d7dbdd;
  height: 6px;
  border-radius: 3px;
}

.player__level::-webkit-slider-thumb {
  -webkit-appearance: none;
  border-radius: 100%;
  background-color: #5c87fe;
  height: 18px;
  width: 18px;
  margin-top: -7px;
}

.audio-duration {
  margin-top: -30px;
  display: flex;
  width: 78%;
  font-size: 10px;
  font-weight: 600;
  color: #a1a1a1;
  letter-spacing: 1px;
}

.start {
  flex: 1;
}

.player__audio {
  visibility: hidden;
}

.player__btn--medium {
  min-height: 70px;
  min-width: 70px;
}

.blue {
  background-color: #5c87fe;
  color: #fff;
}

.hide {
  display: none;
}

</style>