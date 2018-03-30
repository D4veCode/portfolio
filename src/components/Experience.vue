<template>
  <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="experience">
        <div class="my-auto">
          <h2 class="mb-5">Experiencia</h2>
            <experience v-for="(exp, index) in experiences" :exp="exp" :key="index"> </experience>
        </div>

      </section>
</template>
<script>
import Experience from './subcomponents/Exp.vue'

export default {
  name: 'experiences',
  props:['experiences'],
  components: {
      'experience': Experience
  }
}
</script>
<style scoped>

</style>
