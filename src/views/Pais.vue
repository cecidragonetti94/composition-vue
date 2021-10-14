.<template>
  <!-- <h1>Detalle :{{$route.params.nombre}} </h1> -->
<h1> Detalle : {{nombre}} </h1>

</template>

<script>
import {useFetch} from '../hooks/useFetch'
export default {
    props: ['nombre'],
    setup(props){ // para acceder a las props se pone en router props: true
        console.log(props.nombre)

        return {...useFetch(`https://restcountries.eu/rest/v2/name${props.nombre}`)}
    }
}
</script>

<style>

</style>