<template>
    <div>
        <h3>Lista de juegos</h3>
        <ul class="text-left">
            <li v-for="juego in $store.state.juegos" :key="juego.codigo" :style="{ backgroundColor: juego.color }">
                {{ juego.codigo }} | {{ juego.nombre }} | {{ juego.stock }} | {{ juego.precio }}
            </li>
        </ul>
    </div>
</template>

<script>
export default {
}
</script>

<style>

</style>