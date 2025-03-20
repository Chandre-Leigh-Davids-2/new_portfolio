<template>
  <div class="div">
    <!-- Resume Section -->
    <section id="resume" class="resume section">
      <!-- Section Title -->
      <div class="container section-title py-5" data-aos="fade-up">
        <h2 class="text-center">Resume</h2>
        <p class="text-center">
          As an aspiring Full Stack Developer, I am passionate about creating intuitive and dynamic web applications.
          With a strong foundation in both front-end and back-end development, I’m eager to contribute to innovative
          projects and continuously grow my technical skills. Having completed Life Choices Academy’s web development
          bootcamp, I’m enthusiastic about leveraging my skills in real-world applications, both on-site and remotely.
        </p>
      </div>
      <!-- End Section Title -->

      <div class="container py-5">
        <div class="row">
          <!-- Left Column (Summary & Education) -->
          <div class="col-lg-6" data-aos="fade-up" data-aos-delay="100">
            <!-- End Resume Item -->

            <h3 class="resume-title">Education</h3>
            <!-- Timeline Section -->
            <div class="timeline">
              <div class="resume-item timeline-item">
                <h4>Certificate of Completion: Full Stack Web Development</h4>
                <h5>Apr 2024 - Sept 2024</h5>
                <p><em>Life Choices Academy</em></p>
                <p>
                  I studied Full Stack Web Development at Life Choices Academy where I learnt
                  HTML,CSS,JavaScript,Vue.js,MySQL and Node.js. I built most of my foundation in coding through this
                  course as well as developing and improving on my soft skills.
                </p>
              </div>
              <div class="resume-item timeline-item">
                <h4>Bachelor's Certificate</h4>
                <h5>2019 - 2023</h5>
                <p><em>Mondale High School</em></p>
                <p>
                  I studied at Mondale High School, where I was introduced to Coding through one of the teachers. I was
                  part of what was essentially a start up Coding and Robotics Club.
                </p>
              </div>
            </div>
            <div id="resumeBadges" class="mt-5"></div>
            <div class="badges row d-flex justify-content-center" >
              <h4 class="my-5 ">Badges</h4>
              <div class="col-sm-3">
                <div class="img my-2"><img src="../assets/images/Linux.png" alt=""></div>
              </div>
              <div class="col-sm-3">
                <div class="img my-2"><img src="../assets/images/operatingSystems.png" alt=""></div>
              </div>
              <div class="col-sm-3">
                <div class="img my-2 bg"><img src="../assets/images/aws.png" alt=""></div>
              </div>
              <div class="col-sm-3">
                <div class="img my-2 bg"><img src="../assets/images/WordPressBadge.png" alt=""></div>
              </div>
              <div class="col-sm-3">
                <div class="img my-2 bg"><img src="../assets/images/UIUX.png" alt=""></div>
              </div>
              <div class="col-sm-3">
                <div class="img my-2"><img src="../assets/images/JSE2.png" alt=""></div>
              </div>
              <div class="col-sm-3">
                <div class="img my-2"><img src="../assets/images/python.png" alt=""></div>
              </div>
              <div class="col-sm-3">

              </div>
            </div>
            <div class="button my-5">
              <router-link to="/certificates"><button>Certificates</button></router-link>
            </div>

            <!-- End Timeline Section -->
          </div>
          <!-- End Left Column -->

          <!-- Right Column (Professional Experience) -->
          <div class="col-lg-6" data-aos="fade-up" data-aos-delay="200">
            <h3 class="resume-title">Professional Experience</h3>
            <!-- Timeline Section -->
            <div class="timeline">

              <div class="resume-item timeline-item">
                <h4>Software Devloper</h4>
                <h5>Jan 2025 - present</h5>
                <p><em>LC Studio</em></p>
                <ul>
                  <li>
                    I got promoted to a Software Dev intern at LC Studio where I worked on and presented projects with
                    my team. I also worked on a project that involved creating a web application using python and the
                    Flask Framework.
                  </li>
                </ul>
              </div>

              <div class="resume-item timeline-item">
                <h4>Web Devloper</h4>
                <h5>Oct 2024 - Dec 2024</h5>
                <p><em>LC Studio</em></p>
                <ul>
                  <li>
                    I started my learning journey for Web Development at LC Studio where I interned as a Web Developer,
                    worked on and presented projects with my team. I learnt a lot about teamwork, communication and time
                    management. I also learnt about the importance of documentation and testing, Wordpress, SEO and
                    advanced JavaScript.
                  </li>
                </ul>
              </div>

              <div class="resume-item timeline-item">
                <h4>Entrepreneur</h4>
                <h5>Aug 2023 - present</h5>
                <p><em>Prettier is Pink</em></p>
                <ul>
                  <li>
                    I currently have and run my own business where I sell Satin roses and crafts.
                  </li>
                </ul>
              </div>

              <div class="resume-item timeline-item">
                <h4>Filing</h4>
                <h5>Dec 2023 - Mar 2024</h5>
                <p><em>Uppper Edge Pty Ltd</em></p>
                <ul>
                  <li>
                    I casualed as a filing clerk at Upper Edge Pty Ltd. I was responsible for filing documents,
                    answering packing and assisting.
                  </li>
                </ul>
              </div>
            </div>
            <!-- End Timeline Section -->
          </div>
          <!-- End Right Column -->
        </div>
      </div>

    </section>
  </div>
</template>

<script>
export default {
  mounted() {
    this.$nextTick(() => {
      this.initTimeline();
    });
  },
  methods: {
    initTimeline() {
      // You can add extra animations or effects here if needed
    }
  }
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Fredoka:wght@300..700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Fredoka:wght@300..700&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

/* Resume Title */
h2,
h4,
h5 {
  font-family: "Fredoka", serif;
}

p {
  font-family: "Poppins", serif;
}

.resume .resume-title {
  color: var(--heading-color);
  font-size: 26px;
  font-weight: 700;
  margin-top: 20px;
  margin-bottom: 20px;
}

.div {
  background-color: rgb(251, 217, 222);
}

/* Timeline Container */
.timeline {
  position: relative;
  padding-left: 30px;
  /* Space for the timeline line */
  margin-left: 30px;
  border-left: 2px solid var(--accent-color);
}

/* Timeline Item */
.timeline .resume-item {
  position: relative;
  padding-left: 30px;
  margin-bottom: 30px;
}

/* Timeline Dot */
.timeline .resume-item::before {
  content: "";
  position: absolute;
  left: -9px;
  top: 0;
  width: 16px;
  height: 16px;
  background-color: var(--accent-color);
  border-radius: 50%;
  border: 2px solid var(--background-color);
}

/* Timeline Headers */
.timeline .resume-item h4 {
  font-size: 20px;
  font-weight: bold;
  color: var(--default-color);
  margin-bottom: 5px;
}

.timeline .resume-item h5 {
  font-size: 16px;
  font-weight: 600;
  color: var(--heading-color);
  margin-bottom: 10px;
}

.timeline .resume-item ul {
  padding-left: 20px;
}

.timeline .resume-item ul li {
  padding-bottom: 5px;
}

.img {
  width: 70%;
  height: auto;
  margin-left: 5%;
}

.bg {
  background-color: rgba(255, 255, 255, 0.781);
  border-radius: 8px;
}

img {
  height: 100%;
  width: 100%;
  object-fit: contain;
}

button {
  border: none;
  background-color: #E5B80B;
  color: white;
  padding: 15px;
  border-radius: 5px;
}

button:hover {
  border: none;
  color: #E5B80B;
  background-color: white;
  padding: 15px;
  border-radius: 5px;
  transition: 0.2s ease-in-out;
}
</style>