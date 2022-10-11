<template>
    <main>
        <!-- Jumbotron -->
        <section class="d-flex justify-content-center align-items-center" id="jumbotron">
            <div class="jumbo-content">
                <h2>Key to your success</h2>
                <p>EduPrime is the most versatile Wordpress theme for educational purposes, showcasing universities,
                    courses,
                    secondary schools etc.</p>
                <a class="btn-primary" href="#">
                    <i class="fa-solid fa-magnifying-glass"></i>
                    <span>Search courses</span>
                </a>
                <a class="btn-white" href="#">
                    <i class="fa-solid fa-user-plus"></i>
                    <span>Apply for university</span>
                </a>
            </div>
            <img src="../assets/img/Wave-1.png" alt="Wave 1">
        </section>
        <!-- Browse courses  -->
        <section id="browse">
            <div class="container">
                <div class="row">
                    <div class="col-6">
                        <img class="books" src="../assets/img/Books-icon.png" alt="Books icon">
                        <h3>Thousands of courses for any type of student</h3>
                        <p>At EduPrime, it doesn’t matter what domain you wish to pursue a career in. Here you can find
                            a course
                            that
                            satisfies your needs within a click away and applies for a course in a matter of minutes.
                            EduPrime is
                            ranked
                            as the most versatile university in the world, thanks to the number of courses it provides.
                        </p>
                        <MainButton anchor="Browse through courses" url="#" scheme="regular success" />
                    </div>
                    <div class="col-6 d-flex justify-content-center align-items-center">
                        <img class="grad-hat" src="../assets/img/Graduation-Illustration.png" alt="Graduation hat">
                    </div>
                </div>
            </div>
        </section>
        <!-- Faculties  -->
        <section id="faculties">
            <h3>Faculties available at EduPrime</h3>
            <p>A single university with a load of course, tailored to satisfy any student's needs.</p>

            <!-- Importazione Slider -->
            <BoxesSlider :items="facultiesSliderItems" />
            <svg version="1.0" xmlns="http://www.w3.org/2000/svg" width="2954.667" height="186.667"
                viewBox="0 0 2216 140">
                <path class="st0"
                    d="M324.7 34.8c-76.4 51.8-134.1 82-177.2 92.8-12.2 3.1-33.8 4.3-42.8 2.5-8.1-1.7-18.5-7.2-24.2-12.8-5.7-5.7-10.1-12.2-17.4-26.1C57 79.6 52.6 75 47.7 75c-7.9 0-21.2 9.9-37.9 28.3L0 114v26h1105.2c729.3 0 1104.9-.3 1104.2-1-2.6-2.6-29.5-18-42.9-24.5-46.4-22.7-82.1-27.7-122.7-17.5-4.6 1.2-19.1 5.5-32.3 9.5-40.2 12.4-58.5 16.1-85.5 17.2-33.9 1.3-73.5-5.3-117.9-19.9-14.8-4.8-48.5-17.8-59.7-23l-5.2-2.4-16.3 1.8c-125.9 13.6-219.6 20.5-324.9 23.9-40.1 1.3-166.2.6-196-1-71.9-4-119.7-8.4-173.5-16.2-26.8-3.8-69.6-11.2-83.1-14.4-5-1.1-8-1.3-13.2-.5-3.7.5-18.8 2.3-33.7 3.9C793 88.1 702 89.1 622 79c-51.2-6.5-89.6-15.2-150.5-34-35.4-10.9-84.3-20.7-121.8-24.3-3.5-.3-5.6.9-25 14.1z"
                    fill="#DA5F60E6" />
            </svg>
        </section>
        <!-- University Year con lavorazione sulle position nel CSS  -->
        <section class="bg-danger" id="year">
            <div>
                <img class="icon" src="../assets/img/Clock-and-Bell.png" alt="Clock and bell icon">
                <h3>University Year</h3>
                <div>
                    <img src="../assets/img/Timeline-Item.png" alt="Timeline">
                    <div class="timeline-item-wrapper timeline-1">
                        <h6>Orientation</h6>
                        <p>First day of the university year, all students gather for the opening ceremony and then
                            network with
                            others.</p>
                    </div>
                    <div class="timeline-item-wrapper timeline-2">
                        <h6>Demo Classes</h6>
                        <p>In the first week, students try to accommodate with the teaching style and choose their
                            optional
                            courses.</p>
                    </div>
                    <div class="timeline-item-wrapper timeline-3">
                        <h6>Evaluation</h6>
                        <p>At the end of a semester, students take a general evaluation test for every subject they’re
                            learning.
                        </p>
                    </div>
                    <div class="timeline-item-wrapper timeline-4">
                        <h6>Graduation Day</h6>
                        <p>On the day of graduation, all students gather for the ceremony and then network and party
                            among others.
                        </p>
                    </div>
                </div>
            </div>
        </section>
        <!-- Upcoming Events  -->
        <section class="bg-danger" id="upcoming">
            <div>
                <img class="icon" src="../assets/img/upcoming-events-calendar-icon.png" alt="Calendar icon">
                <h3>Upcoming Events</h3>
                <!-- Importazione Card eventi -->
                <EventsCards btn-url="#" :items="eventsItems" />
            </div>
        </section>
        <svg id="wave-upcoming" version="1.0" xmlns="http://www.w3.org/2000/svg" width="2821.333" height="177.333"
            viewBox="0 0 2116 133">
            <path class="st0"
                d="M6 .4c0 .8 22.8 14.1 35.5 20.7 35.6 18.6 68.6 26.7 96.8 23.9 15.1-1.5 29.4-4.8 54.3-12.6 40-12.5 57.6-16.1 84.4-17.1 45.6-1.6 98.7 10.6 160.6 37.1 7.1 3.1 14.2 5.6 15.8 5.6 1.5 0 17.3-1.6 35-3.5 85-9.2 166.6-15.4 259.1-19.7 36.9-1.7 181.6-1.7 215 0 89.4 4.7 163.2 12.9 226.5 25.4 13.3 2.6 24.2 4.3 28.5 4.2 3.9 0 19.4-1.4 34.5-3.2 60.9-7 102.4-9.6 157-9.6 94.2 0 162.8 9.8 244 34.9 44.3 13.6 79.7 21.3 119.4 25.9l13 1.5 30.5-20.3c85.2-56.8 141.9-83.5 181.6-85.3 28.4-1.3 43 7.9 57 35.7 7.9 15.7 12 19.4 19.5 17.1 6.8-2 15.6-8.9 28.9-22.7l13.1-13.6V0H1061C480.8 0 6 .2 6 .4z"
                fill="#DA5F60E6" />
        </svg>
        <!-- Courses  -->
        <section class="container" id="courses">
            <h3>Latest Courses</h3>
            <!-- Importazione Card Corsi -->
            <CoursesCards :items="coursesItems" />
        </section>
        <!-- Infos  -->
        <section class="container" id="infos">
            
        </section>
        <!-- Newsletter  -->
        <section id="newsletter">
            <div class="container">
                <div class="row">
                    <div class="col-7 newsletter-text">Subscribe Now to Our Newsletter!</div>
                    <div class="col-5 newsletter-input">
                        <!-- Importazione Spazio per input -->
                        <BaseInput placeholder="Email address..." icon="fa-paper-plane" />
                    </div>
                </div>
            </div>
        </section>
        <!-- Partners  -->
        <section id="partners">
            <div class="container text-center">
                <h3>Partners</h3>
                <p>Leverage agile frameworks to provide a robust synopsis for high level overviews. Iterative approaches
                    to
                    corporate strategy.
                </p>

                <!-- Immagini partner ciclati tramite ${n} ?? -->
                <div>
                    <img v-for="n in 8" :key="n" class="c-pointer" :src="require(`../assets/img/partner-${n}.png`)"
                        :alt="`Partner ${n}`">
                </div>
                
            </div>
            <div id="partners-bg-img">
            </div>
        </section>
    </main>
</template>


<!-- Importazione componenti -->
<script>
import MainButton from './MainButton.vue';
import BoxesSlider from './BoxesSlider.vue';
import EventsCards from './EventsCards.vue';
import CoursesCards from './CoursesCards.vue';
import BaseInput from './BaseInput.vue';

// Esportazione componenti, questo collegato tramite le props agli array su App.vue
export default {
    name: "MainMain",
    components: { MainButton, BoxesSlider, EventsCards, CoursesCards, BaseInput },
    props: {
        facultiesSliderItems: Array,
        eventsItems: Array,
        coursesItems: Array,
        infosItems: Array,
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/vars';

main {
    #jumbotron {
        height: 800px;
        background-image: url('~@/assets/img/theme_slider2_bg-1.jpg');
        background-size: cover;
        background-repeat: no-repeat;
        background-position: center;
        position: relative;

        &::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            bottom: 0;
            right: 0;
            background-color: $danger;
            filter: opacity(0.9);
        }

        .jumbo-content {
            position: relative;
            width: 700px;
            text-align: center;
            color: #fff;

            h2,
            p {
                margin-bottom: 40px;
            }

            p {
                font-size: 22px;
            }

            a {
                
                display: inline-block;
                padding: 25px 50px;
                border-radius: 40px;
                margin-right: 40px;

                &:last-of-type {
                    margin-right: 0;
                }

                i {
                    margin-right: 10px;
                }
            }
        }

        img {
            position: absolute;
            width: 2300px;
            max-width: 2300px;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
        }
    }

    #browse {
        padding: 150px 0;
        background-image: url('~@/assets/img/home-background.png');
        background-repeat: no-repeat;

        .books {
            height: 60px;
        }

        h3 {
            padding: 20px 0 30px;
        }

        p {
            margin-bottom: 40px;
        }

        .grad-hat {
            height: 400px;
        }
    }

    #faculties {
        padding-top: 50px;
        text-align: center;

        >h3 {
            margin-bottom: 30px;
        }

        >p {
            margin: 0 auto;
            max-width: 350px;
            margin-bottom: 50px;
        }

        svg {
            transform: translateY(5px);
        }
    }

    #year>div,
    #upcoming>div {
        margin: 0 auto;
        max-width: 1100px;
        color: #fff;
        text-align: center;

        h3 {
            margin-bottom: 60px;
        }

        .icon {
            height: 70px;
            margin: 0 auto 20px;
            display: block;
        }
    }

    #year {
        padding: 100px 0 70px;

        h3 {
            display: inline-block;
            background-color: $warning;
        }

        >div {

            >div {
                padding: 110px 0;
                position: relative;

                .timeline-item-wrapper {
                    max-width: 400px;
                    position: absolute;

                    &.timeline-1 {
                        bottom: 0;
                        left: 15px;
                    }

                    &.timeline-2 {
                        top: 10px;
                        left: 240px;
                    }

                    &.timeline-3 {
                        bottom: 0;
                        left: 470px;
                    }

                    &.timeline-4 {
                        top: 10px;
                        left: 690px;
                    }
                }
            }
        }
    }

    #upcoming {
        position: relative;

        >div {
            padding-bottom: 100px;
        }

    }

    #wave-upcoming {
        transform: translateY(-5px);
    }

    #courses {
        margin-bottom: 120px;

        h3 {
            margin-bottom: 50px;
        }
    }

    #infos {
        margin-bottom: 70px;
    }

    #newsletter {
        padding: 70px 0;
        background-color: $danger;

        .newsletter-text {
            font-size: 35px;
            line-height: 70px;
            vertical-align: middle;
            color: #fff;
            
        }
    }

    #partners {

        h3 {
            padding: 40px 0 30px;
        }

        p {
            margin: 0 auto;
            max-width: 550px;
        }


        img {
            height: 50px;
            margin: 30px 20px;
            filter: opacity(0.3);

            &:hover {
                filter: none;
            }
        }

        #partners-bg-img {
            height: 300px;
            background-color: $lightSecondary;
            background-image: url('~@/assets/img/background-wave3.png');
            background-repeat: no-repeat;
        }
    }
}
</style>