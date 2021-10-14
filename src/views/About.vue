<template>
  <div class="about">
    <Title :contador="contador" :color="color"/>
    <h1 :style="{'color': color}">Contador : {{contador}} </h1>
    <!-- <button @click="aumentar">+</button>
    <button @click="disminuir">-</button> -->
    <Btn :textoBoton="'Aumentar'" @accion="aumentar" />
    <Btn :textoBoton="'Disminuir'" @accion="disminuir" />
    <hr>
    <input type="text" v-model="texto">
    <p>{{texto}}</p>

  </div>
</template>

<script>
import { computed, ref } from '@vue/reactivity'
import Title from '../components/Title.vue'
import Btn from '../components/Btn.vue'

export default {
  components: {
    Title,
    Btn
  },


  //se ejecuta antes de que se cree el componente
  setup(){
    const contador = ref(0) //inicializo en 0
    const texto = ref('')

    const aumentar = () => {
      contador.value ++  //accedo al valor que tiene contador
    }
      const disminuir = () => {
      contador.value --  //accedo al valor que tiene contador
    }

    const color = computed(()=>{
      if (contador.value < 0){
        return 'red'
      }else 
      return'green'
    })


    return {contador, aumentar,disminuir,color,texto}
  }
}
</script>
