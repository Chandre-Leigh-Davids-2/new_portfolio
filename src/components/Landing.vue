<template>
    <div>
        <section id="hero" class="hero section light-background d-flex align-content-center div">

            <div class="container" data-aos="zoom-out">
                <div class="row justify-content-center">
                    <div class="col-lg-9">
                        <h1>Chandré Leigh Davids 
                        </h1><br>
                        <span class="txt-type" data-wait="3000">
                            <p class="txt">I am {{ txt }}</p>
                        </span>
                        <div class="box d-flex justify-content-center">
                            <a href="https://github.com/Chandre-Leigh-Davids-2/" target="_blank" class="mx-3"><i
                                    class="bi bi-github"></i></a>
                            <a href="https://www.linkedin.com/in/chandre-leigh-davids-50410a33b" target="_blank"><i
                                    class="bi bi-linkedin"></i></a>
                        </div>
                        <div class="d-flex justify-content-center">
                            <a href="https://chandre-leigh-davids-2.github.io/new_portfolio/src/assets/images/My%20Cv.pdf" target="_blank"><button class="my-3">View My CV</button></a>
                        </div>
                    </div>
                </div>
            </div>

        </section><!-- /Hero Section -->

    </div>
</template>
<script>
export default {
    data() {
        return {
            txt: '',          // The current text being typed
            wordIndex: 0,     // The index for the current word
            isDeleting: false, // If true, characters are being deleted
            words: ['an Aspiring Full Stack Developer','a UI/UX Designer', 'a Web Developer'], // List of words to type
            wait: 3000        // Wait time before deleting the text
        };
    },
    methods: {
        type() {
            const current = this.wordIndex % this.words.length; // Current word index
            const fullTxt = this.words[current]; // Full text of the current word

            if (this.isDeleting) {
                // Remove one character
                this.txt = fullTxt.substring(0, this.txt.length - 1);
            } else {
                // Add one character
                this.txt = fullTxt.substring(0, this.txt.length + 1);
            }

            let typeSpeed = 200; // Default typing speed

            if (this.isDeleting) {
                typeSpeed /= 2; // Slow down when deleting
            }

            if (!this.isDeleting && this.txt === fullTxt) {
                // If the word is fully typed, wait for a moment
                typeSpeed = this.wait;
                this.isDeleting = true;
            } else if (this.isDeleting && this.txt === '') {
                // If the word is deleted, move to the next word
                this.isDeleting = false;
                this.wordIndex++;
                typeSpeed = 300;
            }

            // Call `type` method again after `typeSpeed` ms
            setTimeout(this.type, typeSpeed);
        }
    },
    mounted() {
        // Start typing once the component is mounted
        this.type();
    }
};
</script>
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Fredoka:wght@300..700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Fredoka:wght@300..700&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

h1{
    font-family: "Fredoka", serif;
    font-size: 10vh;
}
p{
    font-family: "Poppins", serif;
}
.div {
    min-height: 100vh;
}
a{
    text-decoration: none;
}
.hero {
    display: flex;
    justify-content: center; /* Centers horizontally */
    align-items: center; /* Centers vertically */
    text-align: center; /* Ensures text is centered */
    min-height: 100vh; /* Full viewport height */
    background-image: url('../assets/images/pexels-mdsnmdsnmdsn-1831234.jpg');
}

.container {
    text-align: center; /* Centers the text inside the container */
}
i{
    color: pink;
    font-size: 5vh;
}
button{
    background-color: pink;
    color: white;
    font-family: "Poppins", serif;
    padding: 10px;
    width: fit-content;
    min-width: 12vw;
    border: none;
    border-radius: 15px ;
}
</style>