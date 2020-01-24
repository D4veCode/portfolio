<template>
  <div id="app">
     <nav class="navbar navbar-expand-lg navbar-dark bg-primary fixed-top" id="sideNav">
      <a class="navbar-brand js-scroll-trigger" href="#page-top">
        <span class="d-block d-lg-none">¡Bienvenido!</span>
        <span class="d-none d-lg-block">
          <img class="img-fluid img rounded-circle mx-auto mb-2" src="./assets/img/ds trans 2.png" alt="">
        </span>
      </a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav">
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#about">About</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#experience">Experiencia</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#education">Educacion</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#skills">Habilidades</a>
          </li>
          <!--<li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#interests">Intereses</a>
          </li>-->
        </ul>
      </div>
    </nav>

    <div class="container-fluid p-0">

     
      <about :about="misdatos"></about>
      <experience :experiences="experiences"></experience>
      <education :education="education"></education>
      <skills :flujo-trabajo="workflow"></skills>
     

      <!---<section class="resume-section p-3 p-lg-5 d-flex flex-column" id="interests">
        <div class="my-auto">
          <h2 class="mb-5">Interests</h2>
          <p>Apart from being a web developer, I enjoy most of my time being outdoors. In the winter, I am an avid skiier and novice ice climber. During the warmer months here in Colorado, I enjoy mountain biking, free climbing, and kayaking.</p>
          <p class="mb-0">When forced indoors, I follow a number of sci-fi and fantasy genre movies and television shows, I am an aspiring chef, and I spend a large amount of my free time exploring the latest technolgy advancements in the front-end web development world.</p>
        </div>
      </section>-->

    </div>
  </div>
</template>


  <!-- Bootstrap core JavaScript -->
    <script src="./assets/vendor/jquery/jquery.min.js"></script>
    <script src="./assets/vendor/bootstrap/js/bootstrap.bundle.min.js"></script>

    <!-- Plugin JavaScript -->
    <script src=".assets/vendor/jquery-easing/jquery.easing.min.js"></script>

    <!-- Custom scripts for this template -->
    <script src="./assets/js/resume.min.js"></script>


<script>
import About from './components/About.vue';
import Experience from './components/Experience.vue'
import axios from 'axios'
import Education from './components/Education.vue'
import Skills from './components/Skills.vue'

export default {
  name: 'app',
  components: {
    'about': About,
    'experience': Experience,
    'education': Education,
    'skills': Skills
  },
  data(){
    return{
      misdatos: {
        name: 'David A.',
        lastname: 'Serrada B.',
        address: 'Caracas, Venezuela',
        phone: '+58(412)615-04-92',
        email: 'davidasb.developer@gmail.com',
        description: 'Desarollador web de 21 años, siempre en busca de aprender nuevas cosas y reforzar las aprendidas. ',
        instagram: 'https://www.instagram.com/davidalejandrosb/',
        twitter: 'https://twitter.com/DavidWrote',
        linkedin: 'https://www.linkedin.com/in/david-serrada-dev/',
        github: 'https://github.com/D4veCode'

      },
      experiences:[
        {job: 'Asistente Drupal', company:'Strategy Plaza', description:'Asistente de la empresa Strategy Plaza, actualiza, crea y modifica sitios web basados en Drupal 8.', date: 'Ene 2018 - Agosto 2018'},
        {job: 'Desarrollador Backend', company: 'YEiPii', description: 'Desarrollador Backend, mis tareas fueron refactorizar algunos componentes en el backend hecho en NodeJS e implementar nuevas funciones.', date: 'Jun 2019- Agosto 2019'}
      
      ],
      education:[{school:'Universidad Católica Andrés Bello', degree:'8vo Semestre de Ingeniería Infomática', date:'Sept 2015 - Presente'},
                {school:'U.E Colegio Valle Alto', degree:'Bachiller en Ciencias', date:'Sept 2010 - Jul 2015'}
      ],
      workflow: {
        first: 'Mobile-First, Diseño Responsivo',
        second: 'Desarrollo Ágil & Scrum',
        third: 'Equipos Funcionales'
      }      
    }
  }
}
</script>

<style>

</style>
