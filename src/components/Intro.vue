<template>
  <div class="intro">
    <div class="intro__container">
      <div class="intro__inner">
        <hgroup class="intro__hg">
          <h1 class="intro__hg__heading">Hey!</h1>
          <h2 class="intro__hg__subheading">Let me introduce myself</h2>
        </hgroup>
        <p>
          I am a creative front-end developer based in
          <a
            href="https://goo.gl/maps/goJXEWFRcLxnSTdW6"
            rel="external"
            target="_blank"
          >Naarden</a>, The Netherlands with over ten years' industry experience.
          I have worked for multiple digital agencies like Poort80, DigitasLBi, eFocus, and Valtech on a wide variety of projects for local and global clients.
        </p>
        <p>My core values are structured code, attention to detail, and an understanding of my clients' needs.</p>
        <p>I love working and discovering new technologies such as CSS Grid level 2, scroll snapping, variable fonts, SVG animation, Vue.js, React and all the cool stuff that ES.Next is bringing us.</p>
        <p>
          I specialize in front-end web development where my interest is more towards the creative part of this discipline.
          I would rather call myself a UI Engineer than a Javascript developer who leans more against the backend part of an application.
          I prefer to work on a nice UI rather than tie up boring business logic.
        </p>
        <p>I really like to use javascript purely for presentation purposes only, therefore I find libraries like GreenSock, Anime.js great to work with, I am also a big fan of Vue.js because this framework perfectly integrates into projects and is easy to combine with other javascript libraries.</p>

        <p>
          Besides coding I love photography, I got my own small business "
          <a
            href="http://plat-vlak.nl/"
            rel="external"
            target="_blank"
          >plat vlak photography</a> started in 2015.
        </p>

        <h3 class="intro__subheading">Current status</h3>
        <p>
          I currently work at
          <a
            href="https://www.deptagency.com/"
            rel="external"
            target="_blank"
          >DEPT Agency</a>, here I work together with several disciplines and together we maintain various platforms.
          We generally work Agile according to the Scrum framework.
        </p>

        <h3 class="intro__subheading">Hobbies</h3>
        <p>In addition to my full-time job as a father of two kids, I like to photograph with my Digital SLR camera and regularly play computer games on my Nintendo switch.</p>
        <p>I have also been discovering a new hobby lately and that is FPV drone racing.</p>
      </div>

      <h2 class="intro__heading">Recent projects</h2>

      <Project :projects="projects"/>

      <h2 class="intro__heading">Work experience</h2>
      <Box :boxes="boxes"/>
    </div>
  </div>
</template>

<script>
import Project from "@/components/Project.vue";
import Box from "@/components/Box.vue";

export default {
  name: "Intro",
  components: {
    Project,
    Box
  },
  data() {
    return {
      boxes: [
        {
          heading: "Front-end developer",
          subheading: "DEPT Agency",
          employed: "Apr 2011 – Present"
        },
        {
          heading: "Front-end developer",
          subheading: "Valtech",
          employed: "Jul 2011 – Mrt 2019 ▪ 7 years 9 months"
        },
        {
          heading: "Front-end developer",
          subheading: "DigitasLBi",
          employed: "Sep 2010 – Jun 2011 ▪ 10 months"
        },
        {
          heading: "Front-end developer",
          subheading: "Poort80",
          employed: "Oct 2006 – Aug 2010 ▪ 3 years 11 months"
        },
        {
          heading: "Internship - Front-end developer",
          subheading: "ICATT interactieve media",
          employed: "Oct 2005 – Sep 2006 ▪ 1 year"
        }
      ],
      projects: [
        {
          heading: "CARU Containers",
          subheading: "www.carucontainers.com",
          url: "https://www.carucontainers.com",
          framework: "Scrum",
          role: "Front-end",
          cms: "Contentful",
          details: [
            {
              heading: "Javascript Frameworks & Libraries",
              items: ["Plain JavaScript", "DEPT front-end shelf", "Anime.js"]
            },
            {
              heading: "CSS Preprocessors & Methodology",
              items: ["Sass", "BEM"]
            },
            {
              heading: "Package Managers & Build tools",
              items: ["NPM", "Gulp"]
            }
          ]
        },
        {
          heading: "Valtech Global Website",
          subheading: "www.valtech.com",
          url: "https://www.valtech.com",
          framework: "Scrum",
          role: "Front-end lead",
          cms: "EpiServer",
          details: [
            {
              heading: "Javascript Frameworks & Libraries",
              items: ["Plain JavaScript", "Vue.js", "GreenSock: GSAP"]
            },
            {
              heading: "CSS Preprocessors & Methodology",
              items: ["Sass", "BEM"]
            },
            {
              heading: "Package Managers & Build tools",
              items: ["NPM", "Gulp"]
            }
          ]
        },
        {
          heading: "Aegon Careers",
          subheading: "careers.aegon.com",
          url: "https://careers.aegon.com",
          framework: "Scrum",
          role: "Front-end lead",
          cms: "EpiServer",
          details: [
            {
              heading: "Javascript Frameworks & Libraries",
              items: ["Plain JavaScript", "Vue.js", "Anime.js"]
            },
            {
              heading: "CSS Preprocessors & Methodology",
              items: ["Sass", "BEM"]
            },
            {
              heading: "Package Managers & Build tools",
              items: ["NPM", "Gulp"]
            }
          ]
        },
        {
          heading: "DURA-ACE",
          subheading: "dura-ace.com",
          url: "https://www.duraace.com",
          framework: "Scrum",
          role: "Front-end",
          cms: "Adobe Experience Manager",
          details: [
            {
              heading: "Javascript Frameworks & Libraries",
              items: ["jQuery", "GreenSock: GSAP", "ScrollMagic"]
            },
            {
              heading: "CSS Preprocessors & Methodology",
              items: ["Sass", "BEM"]
            },
            {
              heading: "Package Managers & Build tools",
              items: ["NPM", "Gulp"]
            }
          ]
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
.intro {
  grid-column: 1;
  grid-row: 2;
  z-index: 1;

  @media screen and (max-width: 1279px) {
    margin-top: 2rem;
  }

  @media screen and (min-width: 1280px) {
    grid-column: 5;
    grid-row: 2;
    position: relative;
    overflow: hidden;
  }

  &__container {
    padding: 0 20px;

    @media screen and (min-width: 1280px) {
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
  }

  &__inner {
    margin-bottom: 4rem;
  }

  &__hg {
    font-family: var(--primary-font);

    @media screen and (max-width: 1279px) {
      color: var(--white);
    }

    &__heading {
      margin: 0;
      font-weight: 700;
      font-size: 1.6rem;

      @media screen and (min-width: 1280px) {
        font-size: 2rem;
      }
    }

    &__subheading {
      margin: 0 0 1rem;
      font-weight: 300;
      font-size: 1rem;

      @media screen and (min-width: 1280px) {
        font-size: 1.2rem;
      }
    }
  }

  p {
    line-height: 1.6;

    @media screen and (max-width: 1279px) {
      color: var(--white);
      font-size: 0.8rem;
    }
  }

  &__heading {
    font-weight: 700;
    font-size: 1.4rem;
    font-family: var(--primary-font);

    @media screen and (max-width: 1279px) {
      color: var(--white);
    }

    @media screen and (min-width: 1280px) {
      font-size: 1.6rem;
    }
  }

  &__subheading {
    margin: 2rem 0 0;
    font-weight: 700;
    font-size: 1.4rem;
    font-family: var(--primary-font);

    @media screen and (max-width: 1279px) {
      color: var(--white);
    }

    @media screen and (min-width: 1280px) {
      font-size: 1.6rem;
    }
  }

  a {
    color: var(--desire);
    text-decoration: none;
  }
}
</style>
