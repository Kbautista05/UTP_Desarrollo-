<template>
  <div id="app">

    <top-banner v-bind:idCarousel="['carousel1']" ></top-banner>

    <div class="container-fluid">

<!-- aquí se deberían cargar 4 películas que simulan las 4 noticias pero el hook no es el correcto -->
          <section-api></section-api>
        </div>

<!-- Esta es la tarjeta de miembros que nos piden pero al parecer estamos enviando las props de mala manera o con un nombre no correcro -->
    <div class="container-fluid">
      <div class="row justify-content-center mb-5">
        <div class="col mt-5" v-for="(item, index) of team" :key="index">
          <team-card :member="item"></team-card>
        </div>
      </div>
    </div>

    <page-footer></page-footer>
    <!-- <h1>{{ title }}</h1> -->
  </div>
</template>

<script>
import PageFooter from "./components/PageFooter.vue";
import TeamCard from "./components/TeamCard.vue";
import SectionApi from "./components/SectionApi.vue";
import TopBanner from './components/TopBanner.vue';

export default {
  name: "App",
  components: {
    PageFooter,
    TeamCard,
    SectionApi,
    TopBanner,
  },
  data(){
    return {
      title: "Galeria PlayaPez",
      carousel1 : 'carousel1',
      // Esta es la definición del objeto team, el objeto contiene la info de cada miembro del equipo
      // Se esta enviando correctamente en el ciclo v-for pero las pruebas fallan
      // Al parecer tenemos un problema con la definición de los nombres de los atributos
      team: [
        {
          codigo: 1,
          nombre: "Jose Angel",
          descripcion:
            "Ingeniero de Telecomunicaciones, CEO de PLAYAPEZ S.A.S, con experiencia en el sector de las TIC´s, trabajo en el desarrollo del Software y hardware electrónico para incrementar la productividad y competitividad del sector piscícola.",
          rol: "Scrum Master",
          imagen: "../assets/Jose.jpeg",
        },
        {
          codigo: 2,
          nombre: "Mayerlin ",
          descripcion:
            "Mayerlin Juliany Jimenez Moreno, 24 años de edad, rol de Product Owner, encargada de representar el cliente ante el equipo y gestionar las soluciones para que el proyecto se desarrole optimamente, ( bueno yo no tengo experiencia en sector las tic pero te diré lo que soy jajja ) Secretaria ejecutiva con 4 años de experiencia como funcionaria pública, estudiante de noveno semestre de administración en salud.",
          rol: "Product Owner",
          imagen: "../assets/Mayerlin.jpeg",
        },
        {
          codigo: 3,
          nombre: "Kevin Bautista",
          descripcion:
            "Tecnólogo en Sistemas con las habilidades necesarias para la adquisición, implementación y puesta en marcha de Tecnología Hardware y Software como solución al mejoramiento y aprovechamiento de los procesos empresariales. Capacidad de investigación, análisis, diagnostico, diseño, construcción, evaluación y mantenimiento de soluciones informáticas mediante la aplicación de tecnologías de información, además de poseer conocimientos prácticos en desarrollo web y diseño gráfico.",
          rol: "Development",
          imagen: "https://placeimg.com/192/192/architecture",
        },
        
      ],
    };
  },
};
</script>