<template>
  <div id="app">
    <!-- Header -->
    <MainHeader :main-menu-items="mainMenuItems" />
    <!-- Main -->
    <MainMain :faculties-slider-items="facultiesSliderItems" :events-items="eventsItems" :courses-items="coursesItems"
      :infos-items="infosItems" />
    <!-- Footer -->
    <MainFooter :categories-labels="CategoriesLabels" :get-edu-menu-items="getEduMenuItems"
      :networking-menu-items="NetworkingMenuItems" />
    
  </div>
</template>

<script>
import MainHeader from './components/MainHeader.vue';
import MainMain from './components/MainMain.vue';
import MainFooter from './components/MainFooter.vue';


export default {
  name: "App",
  data() {
    return {
      hasScrolled: false,

      // ARRAY MENU ORIZZONTALE
      mainMenuItems: [
        {
          id: 1,
          anchor: "Home",
          link: "#",
          
        },
        {
          id: 2,
          anchor: "Courses",
          link: "#",
          
        },
        {
          id: 3,
          anchor: "About Us",
          link: "#",
          
        },
        {
          id: 4,
          anchor: "News",
          link: "#",
          
        },
        {
          id: 5,
          anchor: "Pages",
          link: "#",
          
        },
        {
          id: 6,
          anchor: "Contact",
          link: "#",
          
        },
        {
          id: 7,
          anchor: "Purchase",
          link: "#",
          
        },
      ],

      // ARRAY SLIDER
      facultiesSliderItems: [
        {
          id: 1,
          icon: "Gavel-v2.png",
          img: "Gavel-Illustration-e1556884768193.png",
          title: "Law Faculty",
          text: "Learning from world-leading academics and practitioners, you’ll not only receive an outstanding grounding in the theory of law, but you will be able to understand how those principles are applied in practice through a range of student-led activities and competitions.",
          url: "#",
        },
        {
          id: 2,
          icon: "Coins-tabs-v2.png",
          img: "Economy.png",
          title: "Economy",
          text: "Economics focuses on the behaviour and interactions of economic agents and how economies work. Microeconomics analyzes basic elements in the economy, including individual agents and markets, their interactions, and the outcomes of interactions, including unemployment of resource.",
          url: "#",
        },
        {
          id: 3,
          icon: "Medicine-tabs-v2.png",
          img: "Medicine.png",
          title: "Medicine",
          text: "Medicine is the science and practice of establishing the diagnosis, prognosis, treatment, and prevention of disease. Medicine encompasses a variety of health care practices evolved to maintain and restore health by the prevention and treatment of illness.",
          url: "#",
        },
        {
          id: 4,
          icon: "Computer-tabs-v2.png",
          img: "Computer-Science.png",
          title: "Computer Science",
          text: "Computer science is the study of processes that interact with data and that can be represented as data in the form of programs. It enables the use of algorithms to manipulate, store, and communicate digital information. A computer scientist studies the theory of computation software systems.",
          url: "#",
        },
        {
          id: 5,
          icon: "Palette-tabs-v2.png",
          img: "Graphic-Design.png",
          title: "Graphic Design",
          text: "Graphic design is the process of visual communication and problem-solving through the use of typography, photography and illustration. The field is considered a subset of visual communication and communication design, but sometimes the term ``graphic design`` is used synonymously.",
          url: "#",
        },
      ],

      // ARRAY CARD EVENTI
      eventsItems: [
        {
          id: 1,
          title: "Coaching Sessions",
          date: "20 May 21:30 PM",
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor[...]",
          url: "#",
        },
        {
          id: 2,
          title: "Coaching Sessions",
          date: "24 Mar 18:00 PM",
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor[...]",
          url: "#",
        },
        {
          id: 3,
          title: "Coaching Sessions",
          date: "12 Feb 13:30 PM",
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor[...]",
          url: "#",
        },
      ],

      // ARRAY SCHEDE CORSI
      coursesItems: [
        {
          id: 1,
          icon: "Decisions-icon.png",
          name: "Make Better Decisions",
          teacher: "James Colins",
          price: "$21.00",
          url: "#",
        },
        {
          id: 2,
          icon: "Speaker-icon.png",
          name: "How to be a speaker",
          teacher: "James Colins",
          price: "Free",
          url: "#",
        },
        {
          id: 3,
          icon: "Network-icon.png",
          name: "Network Introductions",
          teacher: "James Colins",
          price: "Free",
          url: "#",
        },
        {
          id: 4,
          icon: "Brand-icon.png",
          name: "Brand Management",
          teacher: "James Colins",
          price: "Free",
          url: "#",
        },
      ],

      // ELENCO VERTICALE MENU FOOTER
      getEduMenuItems: [
        {
          id: 1,
          anchor: "Request a website",
          url: "#",
        },
        {
          id: 2,
          anchor: "Browse Themes",
          url: "#",
        },
        {
          id: 3,
          anchor: "Payment options",
          url: "#",
        },
        {
          id: 4,
          anchor: "Support System",
          url: "#",
        },
        {
          id: 5,
          anchor: "Checkout",
          url: "#",
        },
        {
          id: 6,
          anchor: "Purchase Theme",
          url: "#",
        },
      ],

      // MENU VERTICALE FOOTER
      NetworkingMenuItems: [
        {
          id: 1,
          anchor: "Purchase Theme",
          url: "#",
        },
        {
          id: 2,
          anchor: "Our Benefits",
          url: "#",
        },
        {
          id: 3,
          anchor: "Our Team",
          url: "#",
        },
        {
          id: 4,
          anchor: "Our Services",
          url: "#",
        },
        {
          id: 5,
          anchor: "Other Products",
          url: "#",
        },
        {
          id: 6,
          anchor: "My account",
          url: "#",
        },
      ],

      // ETICHETTE FOOTER
      CategoriesLabels: [
        {
          id: 1,
          anchor: "Economy",
          url: "#",
        },
        {
          id: 2,
          anchor: "Design",
          url: "#",
        },
        {
          id: 3,
          anchor: "Coaching",
          url: "#",
        },
        {
          id: 4,
          anchor: "Business",
          url: "#",
        },
        {
          id: 5,
          anchor: "Medicine",
          url: "#",
        },
        {
          id: 6,
          anchor: "Law",
          url: "#",
        },
        {
          id: 7,
          anchor: "Fitness",
          url: "#",
        },
      ],
    };
  },
  components: {
    MainHeader,
    MainFooter,
    MainMain,
  },
  
 
}
</script>

<style lang="scss">

@import './assets/scss/style.scss';
@import url('https://fonts.googleapis.com/css2?family=Fredoka+One&display=swap');

</style>