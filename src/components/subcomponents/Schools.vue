<template>
   <div class="resume-item d-flex flex-column flex-md-row">
            <div class="resume-content mr-auto">
              <h3 class="mb-0">{{schools.school}}</h3>
              <div class="subheading mb-3">{{schools.degree}}</div>
            </div>
            <div class="resume-date text-md-right">
              <span class="text-primary">{{schools.date}}</span>
              <br>
              <br>
            </div>
          </div>
</template>
<script>
export default {
  name: 'schools',
  props:['schools']
}
</script>
<style>

</style>
