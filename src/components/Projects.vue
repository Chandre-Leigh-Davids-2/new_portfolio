<template>
    <div class="div">
        <section id="portfolio" class="portfolio">
            <div class="container">
                <div class="row text-center pt-5">
                    <h1 class="display-3 fw-bold text-capitalize">Latest work</h1>
                    <div class="heading-line"></div>
                    <p class="lead">
                        "I’m thrilled to showcase my latest projects and can’t wait for you to explore them."
                    </p>
                </div>

                <!-- FILTER BUTTONS -->
                <div class="row mt-5 py-4 g-3 text-center">
                    <div class="col-md-12">
                        <button class="mx-1 btn btn-outline-dark" type="button"
                            @click="filterPortfolio('all')">All</button>
                        <button class="mx-1 btn btn-outline-dark" type="button"
                            @click="filterPortfolio('websites')">Websites</button>
                        <button class="mx-1 btn btn-outline-dark" type="button"
                            @click="filterPortfolio('application')">Application</button>
                        <button class="mx-1 btn btn-outline-dark" type="button" @click="filterPortfolio('case')">Case
                            Studies</button>
                    </div>
                </div>

                <!-- START THE PORTFOLIO ITEMS -->
                <div class="row">
                    <div class="col-lg-4 col-md-6" v-for="(item, index) in filteredItems" :key="index"
                        :data-category="item.category">
                        <div class="portfolio-box shadow">
                            <img :src="item.image" :alt="`portfolio ${index + 1} image`"
                                :title="`portfolio ${index + 1} picture`" class="img-fluid">
                            <div class="portfolio-info">
                                <div class="caption">
                                    <h4>{{ item.title }}</h4>
                                    <p>{{ item.category }} project</p>
                                    <p><a :href="item.url" target="_blank">View Live</a></p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

            </div>
        </section>
    </div>
</template>

<script>
import project1 from '../assets/images/creativePortfolio.png'
import project2 from '../assets/images/pokemon.png'
import project3 from '../assets/images/visio.png'
import project4 from '../assets/images/wordpress.png'
import project5 from '../assets/images/to-do-list.png'
import project6 from '../assets/images/calculator.png'

export default {
    data() {
        return {
            // List of all portfolio items with categories
            portfolioItems: [
                { title: 'Creative Portfolio', category: 'websites', image: project1, url: 'https://portfoliocldavids.vercel.app/' },
                { title: 'Pokedex', category: 'websites', image: project2, url: 'https://pokemon-beta-livid.vercel.app/' },
                { title: 'HTML,CSS,JavaScript', category: 'websites', image: project3, url: 'https://visio-pearl.vercel.app/' },
                { title: 'Wordpress', category: 'websites', image: project4, url: 'https://dev-ecommerce-giftedmoments.pantheonsite.io/' },
                { title: 'To Do List', category: 'application', image: project5, url: 'https://to-do-list-nu-blush.vercel.app/' },
                { title: 'Calculator', category: 'application', image: project6, url: 'https://calculator-peach-iota-86.vercel.app/' },
            ],
            selectedCategory: 'all', // default category
        };
    },
    computed: {
        filteredItems() {
            if (this.selectedCategory === 'all') {
                return this.portfolioItems;
            }
            return this.portfolioItems.filter(item => item.category === this.selectedCategory);
        }
    },
    methods: {
        filterPortfolio(category) {
            this.selectedCategory = category;
        }
    }
};
</script>


<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Fredoka:wght@300..700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Fredoka:wght@300..700&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

h1 {
    font-family: "Fredoka", serif;
}

p {
    font-family: "Poppins", serif;
}

.div {
    min-height: 100vh;
    border: 4px solid #E5B80B;
}

.portfolio {
    padding: 4rem 0;
}

.portfolio button {
    text-transform: capitalize;
}

.portfolio-box {
    position: relative;
    width: 100%;
    height: 18.5rem;
    overflow: hidden;
    margin-bottom: 1.2rem;
    border-top: 1px solid #E5B80B;
}

.portfolio-box img {
    width: 100%;
    height: 100%;
}

.portfolio-box .portfolio-info {
    background-color: #E5B80B;
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    opacity: 0;
    visibility: hidden;
}

.portfolio-box .portfolio-info .caption {
    text-align: center;
    color: #fff;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}

.portfolio-box .portfolio-info .caption h4 {
    text-transform: uppercase;
    display: block;
}

.portfolio-box:hover img {
    transform: scale(1.5);
    transition-duration: 1s;
    transition-property: all;
}

.portfolio-box:hover .portfolio-info {
    opacity: 1;
    visibility: visible;
    transition-duration: 1s;
    transition-property: all;
}

a {
    text-decoration: none;
    color: white;
}

a:hover {
    text-decoration: none;
    color: black;
}
</style>