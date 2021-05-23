<template>
  <div>
    <Error 
    titulo="The page you are looking for does not exist." 
    descripcion="You can click the button below to go back to the home page." 
    boton="Home" />
    <Error 
    titulo="La pagina a la cual intenta acceder no existe" 
    descripcion="De click en el boton para volver al incio." 
    boton="Inicio" />
  </div>
</template>

<script>
// @ is an alias to /src
import Error from '@/components/Error.vue'

export default {
  name: 'Home',
  components: {
    Error
  }
}
</script>
