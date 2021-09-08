<template>
    <div class="busqueda">
        <section>
            <h3>Filtro</h3>
            <input type="text" placeholder="Nombre del juego" :value="$store.state.busqueda" @input="$store.dispatch('setBusqueda', $event.target.value)">
            <ul class="text-left">
                <li v-for="juego in $store.getters.juegosSegunBusqueda" :key="juego.codigo" :style="{ backgroundColor: juego.color }" >
                {{ juego.codigo }} | {{ juego.nombre }} | {{ juego.stock }} | {{ juego.precio }}
                </li>
            </ul>
        </section>
        <section>
            <h3>Cantidad de juegos totales y de stock total</h3>
            <ul class="text-left">
                <li>Juegos totales: {{ $store.state.juegos.length }}</li>
                <li>Stock total: {{ $store.getters.stockTotal }} </li>
            </ul>
        </section>
        <Lista></Lista>
    </div>
</template>

<script>
import Lista from "../components/Lista.vue";
export default {
  components: { Lista },
};
</script>

<style scoped>
.busqueda {
    padding-top: 1em;
}
</style>