<template>
  <div id="app">
     <nav class="navbar navbar-expand-lg navbar-dark bg-primary fixed-top" id="sideNav">
      <a class="navbar-brand js-scroll-trigger" href="#page-top">
        <span class="d-block d-lg-none">¡Bienvenido!</span>
        <span class="d-none d-lg-block">
          <img class="img-fluid img-profile rounded-circle mx-auto mb-2" src="./assets/img/portafolio_i.jpg" alt="">
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
            <a class="nav-link js-scroll-trigger" href="#experience">Experience</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#education">Education</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#skills">Skills</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#interests">Interests</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#awards">Awards</a>
          </li>
        </ul>
      </div>
    </nav>

    <div class="container-fluid p-0">

     
      <about :about="misdatos"></about>
      <experience :experiences="experiences"></experience>
      <education :education="education"></education>
      <skills :flujo-trabajo="workflow"></skills>
     

      <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="interests">
        <div class="my-auto">
          <h2 class="mb-5">Interests</h2>
          <p>Apart from being a web developer, I enjoy most of my time being outdoors. In the winter, I am an avid skiier and novice ice climber. During the warmer months here in Colorado, I enjoy mountain biking, free climbing, and kayaking.</p>
          <p class="mb-0">When forced indoors, I follow a number of sci-fi and fantasy genre movies and television shows, I am an aspiring chef, and I spend a large amount of my free time exploring the latest technolgy advancements in the front-end web development world.</p>
        </div>
      </section>

      <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="awards">
        <div class="my-auto">
          <h2 class="mb-5">Awards &amp; Certifications</h2>
          <ul class="fa-ul mb-0">
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              Google Analytics Certified Developer</li>
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              Mobile Web Specialist - Google Certification</li>
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              1<sup>st</sup>
              Place - University of Colorado Boulder - Emerging Tech Competition 2009</li>
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              1<sup>st</sup>
              Place - University of Colorado Boulder - Adobe Creative Jam 2008 (UI Design Category)</li>
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              2<sup>nd</sup>
              Place - University of Colorado Boulder - Emerging Tech Competition 2008</li>
            <li>
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              1<sup>st</sup>
              Place - James Buchanan High School - Hackathon 2006</li>
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              3<sup>rd</sup>
              Place - James Buchanan High School - Hackathon 2005</li>
          </ul>
        </div>
      </section>

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
  mounted(){
    console.log("Componente cargado...");
    this.getmisdatos();
  },
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
        email: 'davidasb.27@gmail.com',
        description: '',
        instagram: 'https://www.instagram.com/davidalejandrosb/',
        twitter: 'https://twitter.com/DavidWrote',
        linkedin: '',
        github: 'https://github.com/D4veCode'

      },
      experiences:[
        {job: 'Asistente Drupal', company:'Strategy Plaza', description:'Asistente de la empresa Strategy Plaza, actualiza, crea y modifica sitios web basados en Drupal 8.', date: 'Ene 2018 - Presente'},
      
      ],
      education:[{school:'Universidad Católica Andrés Bello', degree:'6to Semestre de Ingeniería Infomática', date:'Sept 2015 - Presente'},
                 {school:'U.E Colegio Valle Alto', degree:'Bachiller en Ciencias', date:'Sept 2010 - Jul 2015'}
      ],
      workflow: {
        first: 'Mobile-First, Responsive Design',
        second: ' Agile Development & Scrum',
        third: 'Cross Functional Teams'
      }

      
    }
  },
  methods: {
    getmisdatos: function(){
      axios.get('http://172.31.38.32:8000/api/about/6')
      .then(res=>{
        console.log(res.data);
        this.misdatos = res.data.datos;
        
      })
      .catch(error=>{
        console.log(error);
      })
    }
  }
 
}
</script>

<style>

</style>
