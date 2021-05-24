<template>
<div>
    <Cabecera />
    <Cuerpo />
</div>
</template>

<script>
// @ is an alias to /src
import Cabecera from '@/components/Cabecera.vue'
import Cuerpo from '@/components/Cuerpo.vue'

export default {
  name: 'Home',
  components: {
    Cabecera,
    Cuerpo
  }
}
</script>
