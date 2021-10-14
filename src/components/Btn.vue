<template>
  <button @click="accionHijo">{{ textoBoton }}</button>
</template>

<script>
export default {
  props:['textoBoton'],
  setup(props,context){
        const accionHijo = (()=> { //el context se usa para poder usar el emit
            context.emit('accion')// esta accion viene del componente padre
        })
        return {accionHijo}
  }
};
</script>

<style>
</style>