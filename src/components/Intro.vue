<template>
  <div class="intro">
    <div class="intro__container">
      <div class="intro__inner">
        <hgroup class="intro__hg">
          <h1 class="intro__hg__heading">Hey! Let me introduce myself</h1>
          <!-- <h2 class="intro__hg__subheading">Creative front-end developer</h2> -->
        </hgroup>
        <p>I am a creative front-end developer based in Naarden, The Netherlands with over ten years' industry experience. I have worked for multiple digital agencies like ICATT, Poort80, eFocus and DigitasLBi on a wide variety of projects for local and global clients.</p>
        <p>I specialize in front-end web development where my interest is more towards the creative part of this discipline. I would rather call myself a creative front-end developer than a "regular front-end developer" who leans more against the backend part of an application. I prefer to work on a nice UI rather then tie up boring business logic.</p>
        <p>My core values are structured code, attention to detail, and an understanding of my clients' needs. I love to work with the newest technologies.</p>
        <p>I worked a lot with Sitecore developers and EpiServer developers many of the projects below are running on these platforms. I have worked less with PHP developers.</p>
        <p>Besides coding I love photography, I got my own business "<a href="http://plat-vlak.nl/" rel="external" target="_blank">plat vlak photography</a> started in 2015.</p>
      </div>

      <h2 class="intro__heading">Recent projects</h2>

      <Project :projects="projects" />

      <h2 class="intro__heading">Work experience</h2>
      <Box :boxes="boxes" />
    </div>
  </div>
</template>

<script>

import Project from '@/components/Project.vue'
import Box from '@/components/Box.vue'

export default {
  name: 'Intro',
  components: {
    Project,
    Box
  },
  data() {
    return {
      boxes: [
        {
          heading: 'Senior - Front-end developer',
          subheading: 'Valtech',
          employed: 'Jul 2011 – Present ▪ 7 years 4 months'
        },
        {
          heading: 'Medior - Front-end developer',
          subheading: 'LBi Lost Boys',
          employed: 'Sep 2010 – Jun 2011 ▪ 10 months'
        },
        {
          heading: 'Junior - Front-end developer',
          subheading: 'Poort80',
          employed: 'Oct 2006 – Aug 2010 ▪ 3 years 11 months'
        },
        {
          heading: 'Stagaire - Front-end developer',
          subheading: 'ICATT interactieve media',
          employed: 'Oct 2005 – Sep 2006 ▪ 1 year'
        }
      ],
      projects: [
        {
          heading: 'Valtech Global Website',
          subheading: 'www.valtech.com',
          url: 'https://www.valtech.com',
          methodology: 'Scrum',
          role: 'Front-end lead',
          cms: 'EpiServer',
          details: [
            {
              heading: 'Javascript Frameworks & Libraries',
              items: ['Plain JavaScript', 'Vue.js', 'GreenSock: GSAP']
            },
            {
              heading: 'CSS Preprocessors & Methodology',
              items: ['Sass', 'BEM']
            },
            {
              heading: 'Package Managers & Build tools',
              items: ['NPM', 'Gulp']
            }
          ]
        }, {
          heading: 'Aegon Careers',
          subheading: 'careers.aegon.com',
          url: 'https://careers.aegon.com',
          methodology: 'Scrum',
          role: 'Front-end lead',
          cms: 'EpiServer',
          details: [
            {
              heading: 'Javascript Frameworks & Libraries',
              items: ['Plain JavaScript', 'Vue.js', 'Anime.js']
            },
            {
              heading: 'CSS Preprocessors & Methodology',
              items: ['Sass', 'BEM']
            },
            {
              heading: 'Package Managers & Build tools',
              items: ['NPM', 'Gulp']
            }
          ]
        }, {
          heading: 'DURA-ACE',
          subheading: 'dura-ace.com',
          url: 'https://www.duraace.com',
          methodology: 'Scrum',
          role: 'Front-end',
          cms: 'Adobe Experience Manager',
          details: [
            {
              heading: 'Javascript Frameworks & Libraries',
              items: ['jQuery', 'GreenSock: GSAP', 'ScrollMagic']
            },
            {
              heading: 'CSS Preprocessors & Methodology',
              items: ['Sass', 'BEM']
            },
            {
              heading: 'Package Managers & Build tools',
              items: ['NPM', 'Gulp']
            }
          ]
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.intro {
  grid-column: 5;
  grid-row: 2;
  position: relative;
  overflow: hidden;

  &__container {
    padding: 0 20px;
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: -17px;
    overflow-y: auto;
    overflow-x: hidden;
    overscroll-behavior: contain;
    -webkit-overflow-scrolling: touch;
  }

  &__inner {
    margin-bottom: 4rem;
  }

  &__hg {
    font-family: var(--primary-font);

    &__heading {
      margin: 0;
      font-weight: 700;
      font-size: 2rem;
    }

    &__subheading {
      margin: 0 0 1rem;
      font-weight: 300;
      font-size: 1rem;
    }
  }

  &__heading {
    font-weight: 700;
    font-size: 1.6rem;
    font-family: var(--primary-font);
  }

  a {
    color: var(--desire);
    text-decoration: none;
  }
}

</style>
