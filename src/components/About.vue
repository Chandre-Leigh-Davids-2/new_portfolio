<template>
  <div class="div">
    <main class="main">

      <!-- About Section -->
      <section id="about" class="about section">

        <!-- Section Title -->
        <div class="container section-title py-5" data-aos="fade-up">
          <h2 class="text-center">About</h2>
          <p class="text-center">Hi, I’m Chandré Leigh Davids, an aspiring Full Stack Developer with a passion for
            coding, hiking, and learning new languages. When I'm not building web apps, you’ll find me exploring the
            outdoors or diving into Mandarin and Korean. Always excited to learn and grow!</p>
        </div><!-- End Section Title -->

        <div class="container" data-aos="fade-up" data-aos-delay="100">

          <div class="row gy-4 justify-content-center">
            <div class="col-lg-4">
              <div class="img">
                <img src="../assets/images/pictureOfSelf.png" class="img-fluid" alt="picture of myself">
              </div>
            </div>
            <div class="col-lg-8 content">
              <h2>UI/UX Designer &amp; Web Developer.</h2>
              <p class="fst-italic py-3">
                Crafting seamless, user-centered designs and building responsive, intuitive web experiences
              </p>
              <div class="row">
                <div class="col-lg-6">
                  <ul>
                    <li><i class="bi bi-chevron-right"></i> <strong>Website:</strong> <span><a
                          href="https://portfoliocldavids.vercel.app/"
                          target="_blank">https://portfoliocldavids.vercel.app/</a></span></li>
                    <li><i class="bi bi-chevron-right"></i> <strong>Phone:</strong> <span>+27 73 325 3129</span></li>
                    <li><i class="bi bi-chevron-right"></i> <strong>City:</strong> <span>Cape Town. South Africa</span>
                    </li>
                  </ul>
                </div>
                <div class="col-lg-6">
                  <ul>
                    <li><i class="bi bi-chevron-right"></i> <strong>Credentials:</strong> <span> <a href="#resumeBadges">View Badges</a></span></li>
                    <li><i class="bi bi-chevron-right"></i> <strong>Email:</strong>
                      <span>chandreleighdavids.17@gmail.com</span>
                    </li>
                    <li><i class="bi bi-chevron-right"></i> <strong>Status:</strong> <span>Open To Work</span></li>
                  </ul>
                </div>
              </div>
              <p class="py-3">
                I currently reside in Rocklands, Mitchell's Plain, and recently completed the Web Development Bootcamp
                at Life Choices Academy, where I was awarded a certificate for my dedication and hard work. This
                experience not only honed my web development skills but also deepened my passion for creating innovative
                and user-friendly websites. I am now actively seeking opportunities and am open to both on-site and
                remote work, eager to collaborate on exciting projects and continue growing as a developer.
              </p>
            </div>
          </div>

        </div>

      </section><!-- /About Section -->

      <!-- Skills Section -->
      <section id="skills" class="skills section">

        <!-- Section Title -->
        <div class="container section-title" data-aos="fade-up">
          <h2>Technical Skills</h2>
          <p>My technical skills include proficiency in HTML, CSS, JavaScript, and basic knowledge of frameworks like
            React. I'm always eager to learn more and expand my skill set, whether it's diving deeper into backend
            development or exploring new tools and technologies to enhance my projects.</p>
        </div><!-- End Section Title -->
        <div class="row d-flex justify-content-center x" data-aos="fade-up" data-aos-delay="100">
          <div class="skill col-sm-2"><img src="../assets//images/html-5.png" alt=""></div>
          <div class="skill col-sm-2"><img src="../assets//images/css.png" alt=""></div>
          <div class="skill col-sm-2"><img src="../assets//images/github.png" alt=""></div>
          <div class="skill col-sm-2"><img src="../assets//images/vuejs.png" alt=""></div>
          <div class="skill col-sm-2"><img src="../assets//images/node.png" alt=""></div>
          <div class="skill col-sm-2"><img src="../assets//images/mySQL.png" alt=""></div>
          <div class="skill col-sm-2"><img src="../assets//images/wordpressIcon.png" alt=""></div>
          <div class="skill col-sm-2"><img src="../assets//images/seo-search-symbol.png" alt=""></div>
          <div class="skill col-sm-2"><img src="../assets//images/pythonIcon.png" alt=""></div>
          <div class="skill col-sm-2"><img src="../assets//images/c-.png" alt=""></div>
        </div>
        <div class="container section-title" data-aos="fade-up">
          <h2>Soft Skills</h2>
          <p>I excel in communication, problem-solving, and teamwork. I’m adaptable and thrive in collaborative
            environments, always open to feedback and eager to improve. I’m committed to fostering positive
            relationships and ensuring tasks are completed efficiently while maintaining a strong attention to detail.
          </p>
          <div class="container-fluid" data-aos="fade-up" data-aos-delay="100">
          <ul>
            <li><i class="bi bi-chevron-right"></i>Disciplined</li>
            <li><i class="bi bi-chevron-right"></i>Orderly</li>
            <li><i class="bi bi-chevron-right"></i>Dedicated</li>
            <li><i class="bi bi-chevron-right"></i>Collaborative</li>
            <li><i class="bi bi-chevron-right"></i>Adaptable</li>
            <li><i class="bi bi-chevron-right"></i>Inquisitive</li>
          </ul>
        </div>
        </div><!-- End Section Title -->

        

      </section><!-- /Skills Section -->


    </main>

  </div>
</template>
<script>
export default {

}
</script>
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Fredoka:wght@300..700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Fredoka:wght@300..700&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

.img {
  width: 80%;
}

img {
  width: 100%;
  object-fit: contain;
}

.div {
  min-height: 100vh;
  border: 4px solid #E5B80B;
}

ul li {
  list-style: none;
}

i {
  color: pink;
}

h2 {
  font-family: "Fredoka", serif;
}

p {
  font-family: "Poppins", serif;
}

.x {
  padding: 5% 12% 5% 12%;
}

.skill {
  width: 9vw;
}

@media screen and (max-width:645px) {
  .skill {
    width: 15vw;
  }
}
</style>