<template>
  <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="education">
        <div class="my-auto">
          <h2 class="mb-5">Education</h2>

        <schools v-for="(schools, index) in education" :schools="schools" :key="index"></schools>
         

        </div>
      </section>
</template>
<script>
import Schools from './subcomponents/Schools.vue'

export default {
  name: 'education',
  props: ['education'],
  components: {
      'schools': Schools
  }
}
</script>
<style>

</style>
