<template>
  <div>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav">
                <li class="nav-item active">
                     <router-link class="nav-link" :to="{name: 'inicio'}">Inicio</router-link>
                </li>
                <li class="nav-item active">
                    <router-link class="nav-link" :to="{name: 'busquedas'}">Búsquedas</router-link>
                </li>
                <li class="nav-item active">
                    <router-link class="nav-link" :to="{name: 'ventas'}">Ventas</router-link>
                </li>
                <li class="nav-item active">
                    <router-link class="nav-link" :to="{name: 'total'}">Total</router-link>
                </li>
            </ul>
        </div>

    </nav>
  </div>
</template>

<script>
export default {
}
</script>

<style>

</style>