<template>
  <section class="home-main">
    <div class="home-main__split home-main__split--left">
      <span class="home-main__small-text">scroll down</span>
    </div>
    <div class="home-main__middle">
      <img src="https://i.ibb.co/HqXFb4c/bottle.png" alt="Cerveza Corona Extra" class="home-main__img" />
    </div>
    <div class="home-main__split home-main__split--right">
      <h1 class="home-main__title">this is living</h1>
      <div class="text-container">
        <p class="home-main__description">
          Born in México and brought up on the beach, Corona is the perfect compliment to
          life's simple pleasures. The golden colour, light refreshing flavor and iconic hand
          pointed bottle, topped off with a refreshly squeezed lime. When the living is
          easy, the beer is Corona.
        </p>
      </div>
    </div>
  </section>
</template>

<script>
export default {

}
</script>

<style lang="scss">

.home-main {
  display: flex;
  &__split {
    width: 50%;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
  }
  &__split--left {
    background: url("https://i.ibb.co/FHFDB8Q/bg-left.jpg") var(--split-left) no-repeat
      center / cover;
    justify-content: flex-end;
  }
  &__small-text {
    color: #000;
    text-transform: uppercase;
    font-size: 0.85em;
    position: absolute;
    bottom: 30%;
    left: 8%;
    transform: rotate(-90deg);
  }
  &__small-text::before {
    content: "";
    position: absolute;
    border: 1px solid #000;
    width: 40px;
    top: 9px;
    left: -50%;
  }
  &__split--right {
    background-color: var(--split-right);
    align-items: center;
    justify-content: center;
  }
  &__title,
  &__description {
    display: none;
  }
  &__middle {
    position: absolute;
    width: 100px;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }
  &__img {
    filter: drop-shadow(15px 10px 50px #000);
  }
}
@media screen and (min-width: 64em) {
  .home-main{
    &__middle {
      width: 130px;
    }
    &__title,
    &__description {
      display: block;
    }
    &__title {
      font-size: 4em;
      text-transform: uppercase;
    }
  }
  .text-container {
    width: 25em;
    text-align: justify;
    font-weight: 400;
    padding: 0;
  }
}
</style>