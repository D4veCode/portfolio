<template>
   <section class="resume-section p-3 p-lg-5 d-flex d-column" id="about">
        <div class="my-auto">
          <h1 class="mb-0">{{about.name}}
            <span class="text-primary">{{about.lastName}}</span>
          </h1>
          <div class="subheading mb-5">{{about.address}}· {{about.phone}} ·
            <a href="mailto:${about.email}" target="blank">{{about.email}}</a>
          </div>
          <p class="mb-5">I am experienced in leveraging agile frameworks to provide a robust synopsis for high level overviews. Iterative approaches to corporate strategy foster collaborative thinking to further the overall value proposition.</p>
          <ul class="list-inline list-social-icons mb-0">
            <li class="list-inline-item"  v-if="about.instagram != ''">
              <a :href="about.instagram" target="blank">
                <span class="fa-stack fa-lg">
                  <i class="fa fa-circle fa-stack-2x"></i>
                  <i class="fa fa-instagram fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>
            <li class="list-inline-item" v-if="about.twitter != ''">
              <a :href="about.twitter" target="blank">
                <span class="fa-stack fa-lg">
                  <i class="fa fa-circle fa-stack-2x"></i>
                  <i class="fa fa-twitter fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>
            <li class="list-inline-item" v-if="about.linkedin != ''">
              <a href="#">
                <span class="fa-stack fa-lg">
                  <i class="fa fa-circle fa-stack-2x"></i>
                  <i class="fa fa-linkedin fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>
            <li class="list-inline-item" v-if="about.github != ''">
              <a :href="about.github" target="blank">
                <span class="fa-stack fa-lg">
                  <i class="fa fa-circle fa-stack-2x"></i>
                  <i class="fa fa-github fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>
          </ul>
        </div>
      </section>
</template>
<script>
export default {
  name: 'About',
  props: ['about'],
  data(){

  }
}
</script>
