<template>
    <div>
        <h2>Total de Ventas</h2>
        <section>
            <h3>Lista total de ventas</h3>
            <ul class="text-left">
                <li v-for="juego in $store.state.ventas" :key="juego.codigo" :style="{ backgroundColor: juego.color }" >
                {{ juego.codigo }} | {{ juego.nombre }} | {{ juego.stock }} | {{ juego.precio }}
                </li>
            </ul>
        </section>
        <section>
            <h3>Monto total de ventas</h3>
            <p>Total: ${{ $store.getters.montoTotalDeVentas }}</p>
        </section>
    </div>
</template>

<script>
export default {
}
</script>

<style>

</style>