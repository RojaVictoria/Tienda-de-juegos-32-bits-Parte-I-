<template>
  <div>
      <h2>Venta de Juegos</h2>
      <section>
            <h3>Cantidad de juegos con stock</h3>
            <ul class="text-left">
            <li v-for="juego in $store.getters.juegosConStock" :key="juego.codigo" :style="{ backgroundColor: juego.color }">
                {{ juego.codigo }} | {{ juego.nombre }} | {{ juego.stock }} | {{ juego.precio }}
            </li>
        </ul>
            <p>Total de juegos con stock: {{ $store.getters.totalJuegosConStock }}</p>
      </section>
      <section>
            <h3>Venta de juegos</h3>
            <ul>
                <li v-for="juego in $store.getters.juegosConStock" :key="juego.codigo">
                    {{juego.nombre}} | Stock: {{juego.stock}} |
                    <input type="button" value="Vender" @click="vender(juego)">
                </li>
            </ul>
      </section>
  </div>
</template>

<script>
export default {
    methods: {
        vender(juego){
            this.$store.dispatch('venderJuego', juego)
        },
    }
}
</script>

<style>
</style>