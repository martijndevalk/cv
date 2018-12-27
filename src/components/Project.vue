<template>
  <div class="projects">
    <div v-for="(project, index) in projects" :key="index" class="project">
      <div class="project__intro">
        <hgroup class="project__hg">
          <h3 class="project__heading">{{ project.heading }}</h3>
          <h4 class="project__subheading">
            <a :href="project.url" rel="external" target="_blank">
              {{ project.subheading }}
              <svg viewBox="0 0 26.01 26.01"><path d="M24.98 0a.832.832 0 0 0-.111.01H17a1 1 0 0 0-.028 2h5.614L10.292 14.303a1 1 0 1 0 1.387 1.441l.027-.027L24 3.424V9.01a1 1 0 0 0 2 .028V1.137A1 1 0 0 0 24.98 0z"/><path d="M11 4.01c-2.496 0-4.382-.004-5.885.166s-2.706.527-3.566 1.389S.335 7.627.166 9.129 0 12.517 0 15.01c0 2.494-.002 4.38.17 5.883s.534 2.704 1.397 3.565c.863.86 2.063 1.217 3.565 1.387s3.382.165 5.868.165 4.368.001 5.869-.17 2.704-.53 3.566-1.391 1.221-2.062 1.393-3.565S22 17.499 22 15.01a1 1 0 0 0-2-.028v.028c0 2.487-.009 4.342-.158 5.648-.15 1.306-.425 1.982-.82 2.377s-1.071.67-2.377.818-3.16.157-5.645.157-4.339-.007-5.645-.154c-1.306-.148-1.982-.421-2.377-.814s-.671-1.07-.82-2.377S2 17.502 2 15.01s.006-4.349.152-5.656.421-1.983.813-2.375 1.067-.667 2.375-.814C6.648 6.017 8.505 6.01 11 6.01a1 1 0 0 0 .028-2H11z"/></svg>
            </a>
          </h4>
        </hgroup>

        <h6 class="project__preheading">Project details</h6>
        <ul class="project__overview-list">
          <li><strong>CMS:</strong> {{ project.cms }}</li>
          <li><strong>Agile framework:</strong> {{ project.framework }}</li>
          <li><strong>My role:</strong> {{ project.role }}</li>
        </ul>

        <div class="project__more-info" @click="showDetails">
          <svg viewBox="0 0 95 55"><polygon points="0,7.5 7.6,0 47.5,39.9 87.4,0 95,7.5 47.5,55 "/></svg>
        </div>
      </div>

      <div class="project__detail">

        <div class="project__detail__item" v-for="(detail, index) in project.details" :key="index">
          <h5 class="project__detail__heading">{{ detail.heading }}</h5>
          <ul class="project__list">
            <li v-for="(item, index) in detail.items" :key="index">
              {{ item }}
            </li>
          </ul>
        </div>

      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: 'Project',
  props: {
    projects: {
      type: Array,
      required: true
    }
  },
  data () {
    return {
      details: false
    }
  },
  methods: {
    showDetails (e) {
      const elm = e.target.parentElement.nextSibling
      e.target.remove();
      elm.classList.add('is-active')
    }
  }
}
</script>

<style lang="scss" scoped>
.project {
  margin: 0 0 2rem;
  padding: 2rem;
  background-color: var(--white);
  box-shadow: 0 0 20px rgba(0,0,0, 0.2);

  @media screen and (min-width: 1280px) {
    margin: 0 0 3rem;
    width: calc(100% - 20px);
  }

  &__hg {
    font-family: var(--secondary-font);
  }

  &__heading {
    margin: 0 0 0.2rem;
    font-weight: 900;
    font-size: 1rem;
    text-transform: uppercase;
    display: inline-block;

    @media screen and (min-width: 1280px) {
      font-size: 1.2rem;
    }
  }

  &__subheading {
    margin: 0 0 1rem;
    font-weight: 300;
    font-size: 0.8rem;

    a {
      color: inherit;
      text-decoration: none;
    }

    svg {
      height: 10px;
    }
  }

  &__more-info {
    padding: 1rem 1rem 0;
    display: flex;
    justify-content: center;
    fill: var(--medium-gray);
    cursor: pointer;

    svg {
      width: 20px;
      height: 20px;
      pointer-events: none;
    }
  }

  &__preheading {
    margin: 0 0 0.2rem;
    font-weight: 700;
    font-size: 0.8rem;
    display: inline-block;

    @media screen and (min-width: 1280px) {
      font-size: 1rem;
    }
  }

  &__detail {
    height: 0;
    overflow: hidden;

    &.is-active {
      margin-top: 2rem;
      height: auto;
    }

    &__heading {
      margin: 0;
      font-weight: 700;
      font-size: 0.8rem;
      display: inline-block;
    }
  }

  &__list {
    margin: 0.5rem 0 2rem;
    padding-left: 20px;

    li {
      font-size: 0.8rem;
      line-height: 1.8;
    }
  }

  &__overview-list {
    margin: 0.5rem 0 0;
    padding-left: 0;

    li {
      list-style: none;
      font-size: 0.8rem;
      line-height: 1.8;
    }
  }

}

</style>
