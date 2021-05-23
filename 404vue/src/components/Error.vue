<template>
  <div class="section-error">
    <p class="section-error-container">
      <span class="section-error-container-num">4</span>
      <i class="far fa-question-circle section-error-container-center"></i>
      <span class="section-error-container-num">4</span>
    </p>
    <p class="section-error-titulo">{{ titulo }}</p>
    <p class="section-error-descripcion">
      {{ descripcion }}
    </p>
    <button class="section-error-boton">{{boton}}</button>
  </div>
</template>

<script>
export default {
  props:{
    titulo: String,
    descripcion: String,
    boton: String,
  }
}
</script>

<style lang="scss">

  @keyframes rotateAnimation {
    from {
      transform: rotate(0);
    }
    to {
      transform: rotate(360deg);
    }
  }

  .section-error{
    margin: 15px;
    &-container{
      letter-spacing: 10px;
      margin-bottom: 20px;
      text-shadow: 7px 7px 0 rgba(0, 0, 0, 0.2);
      font-size: 7em;
      &-center{
        color: #5881b1;
        text-shadow: 5px 5px 0 rgba(0, 0, 0, 0.2);
        animation: rotateAnimation 2s alternate-reverse infinite;
      }
    }
    &-titulo,
    &-descripcion{
      font-size: 1.1em;
    }
    &-titulo{
      text-transform: uppercase;
      margin-bottom: 10px;
    }
    &-boton{
      background-color: transparent;
      outline: none;
      border: 2px solid #5881b1;
      padding: 12px 48px;
      margin: 32px;
      font-size: 1.3em;
      letter-spacing: 1px;
      text-transform: uppercase;
      cursor: pointer;
      transition: box-shadow 0.3s;
      &:hover{
        background-color: #1a2738;
        box-shadow: 4px 4px 0 rgba(0, 0, 0, 0.2);
      }
    }
  }
</style>