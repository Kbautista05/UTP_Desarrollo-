<template>
<div>

<top-menu></top-menu>

    <div v-bind:id="idCarousel" class="carousel slide" data-ride="carousel">
    <ol class="carousel-indicators">
        <li v-bind:data-target="'#' + idCarousel" data-slide-to="0" class="active"></li>
        <li v-bind:data-target="'#' + idCarousel" data-slide-to="1" class=""></li>
        <li v-bind:data-target="'#' + idCarousel" data-slide-to="2" class=""></li>
    </ol>
    <div class="carousel-inner">
        <div class="carousel-item active">
<img src="../assets/central.jpeg" alt="banner image">
            <div class="carousel-caption d-none d-md-block">
                <h5>DEL AGUA A TU MESA</h5>
                <p>Producción y comercialización de kilogramo de Tilapia Roja, entera y sin vísceras, en presentación de 3 unidades de tilapia. Venta de Pescado fresco, cultivado naturalmente en tanques de geomembrana. Libre de productos químicos. Nuestra empresa es 100% responsable con el medio ambiente y ante las normativas nacionales.</p>
            </div>
        </div>
        <div class="carousel-item">
<img src="../assets/Peces.jpeg" alt="banner image">
            <div class="carousel-caption d-none d-md-block">
                <h5>DEL AGUA A TU MESA</h5>
                <p>Producción y comercialización de kilogramo de Tilapia Roja, entera y sin vísceras, en presentación de 3 unidades de tilapia. Venta de Pescado fresco, cultivado naturalmente en tanques de geomembrana. Libre de productos químicos. Nuestra empresa es 100% responsable con el medio ambiente y ante las normativas nacionales.</p>
            </div>
        </div>
        <div class="carousel-item">
<img src="../assets/Tanque.jpeg" alt="banner image">
            <div class="carousel-caption d-none d-md-block">
                <h5>DEL AGUA A TU MESA</h5>
                <p>Producción y comercialización de kilogramo de Tilapia Roja, entera y sin vísceras, en presentación de 3 unidades de tilapia. Venta de Pescado fresco, cultivado naturalmente en tanques de geomembrana. Libre de productos químicos. Nuestra empresa es 100% responsable con el medio ambiente y ante las normativas nacionales.</p>
            </div>
        </div>
    </div>
    <a class="carousel-control-prev" :href="'#' + idCarousel" role="button" data-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="sr-only">Previous</span>
    </a>
    <a class="carousel-control-next" :href="'#' + idCarousel" role="button" data-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="sr-only">Next</span>
    </a>
</div>

</div>
</template>

<script>
import TopMenu from './TopMenu';

export default {
  name: "TopBanner",
  components:{
      TopMenu
  },
  props: ['idCarousel']
};
</script>

<style scoped>
.idCarousel {
            width: 100%;
            display: flex;
            
        }

.carousel-item>img {
    margin-top: 40px;
            width: 100%;
            height: 600px;
            max-width: 1400px;
            object-fit: cover;
        }
</style>