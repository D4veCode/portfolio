<template>
   <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="skills">
        <div class="my-auto">
          <h2 class="mb-5">Habilidades</h2>

          <div class="subheading mb-3">Lenguajes de Programación &amp; Herramientas</div>
          <ul class="list-inline list-icons">
            <li class="list-inline-item">
              <i class="devicons devicons-html5"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-css3"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-javascript_badge"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-jquery"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-nodejs"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-java"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-bootstrap"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-react"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-npm"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-python"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-laravel"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-postgresql"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-mongodb"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-heroku"></i>
            </li>
          </ul>

          <div class="subheading mb-3">Flujo de Trabajo</div>
          <ul class="fa-ul mb-0">
            <li>
              <i class="fa-li fa fa-check"></i>
              {{flujoTrabajo.first}}
            </li>
            <li>
              <i class="fa-li fa fa-check"></i>
              {{flujoTrabajo.second}}
            </li>
            <li v-if="flujoTrabajo.third != ''">
              <i class="fa-li fa fa-check"></i>
              {{flujoTrabajo.third}}
            </li>
          </ul>
        </div>
      </section>
</template>
<script>
export default {
  name: 'skills',
  props: ['flujoTrabajo']
}
</script>
<style>

</style>
