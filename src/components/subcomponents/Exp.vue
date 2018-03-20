<template>
   <div class="resume-item d-flex flex-column flex-md-row mb-5">
            <div class="resume-content mr-auto">
              <h3 class="mb-0">{{exp.job}}</h3>
              <div class="subheading mb-3">{{exp.company}}</div>
              <p>{{exp.description}}</p>
            </div>
            <div class="resume-date text-md-right">
              <span class="text-primary">{{exp.date}}</span>
            </div>
          </div>
</template>
<script>
export default {
  name: 'exp',
  props: ['exp']
}
</script>
