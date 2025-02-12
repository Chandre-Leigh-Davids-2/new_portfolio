<template>
    <div class="div">
      <!-- Resume Section -->
      <section id="resume" class="resume section">
        <!-- Section Title -->
        <div class="container section-title py-5" data-aos="fade-up">
          <h2 class="text-center">Resume</h2>
          <p class="text-center">
            As an aspiring Full Stack Developer, I am passionate about creating intuitive and dynamic web applications. With a strong foundation in both front-end and back-end development, I’m eager to contribute to innovative projects and continuously grow my technical skills. Having completed Life Choices Academy’s web development bootcamp, I’m enthusiastic about leveraging my skills in real-world applications, both on-site and remotely.
          </p>
        </div>
        <!-- End Section Title -->
  
        <div class="container my-5">
          <div class="row">
            <!-- Left Column (Summary & Education) -->
            <div class="col-lg-6" data-aos="fade-up" data-aos-delay="100">
              <h3 class="resume-title">Summary</h3>
              <div class="resume-item timeline-item pb-0">
                <h4>Chandré Leigh Davids</h4>
                <p>
                  <em>
                    Innovative and deadline-driven Graphic Designer with 3+ years of experience 
                    designing and developing user-centered digital/print marketing material from 
                    initial concept to final, polished deliverable.
                  </em>
                </p>
                <ul>
                  <li>Portland par 127, Orlando, FL</li>
                  <li>(123) 456-7891</li>
                  <li>alice.barkley@example.com</li>
                </ul>
              </div>
              <!-- End Resume Item -->
  
              <h3 class="resume-title">Education</h3>
              <!-- Timeline Section -->
              <div class="timeline">
                <div class="resume-item timeline-item">
                  <h4>Master of Fine Arts &amp; Graphic Design</h4>
                  <h5>2015 - 2016</h5>
                  <p><em>Rochester Institute of Technology, Rochester, NY</em></p>
                  <p>
                    Qui deserunt veniam. Et sed aliquam labore tempore sed quisquam iusto autem sit. 
                    Ea vero voluptatum qui ut dignissimos deleniti nerada porti sand markend.
                  </p>
                </div>
  
                <div class="resume-item timeline-item">
                  <h4>Bachelor of Fine Arts &amp; Graphic Design</h4>
                  <h5>2010 - 2014</h5>
                  <p><em>Rochester Institute of Technology, Rochester, NY</em></p>
                  <p>
                    Quia nobis sequi est occaecati aut. Repudiandae et iusto quae reiciendis et quis Eius vel 
                    ratione eius unde vitae rerum voluptates asperiores voluptatem Earum molestiae.
                  </p>
                </div>
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
                  <h4>Senior Graphic Design Specialist</h4>
                  <h5>2019 - Present</h5>
                  <p><em>Experion, New York, NY</em></p>
                  <ul>
                    <li>
                      Lead in the design, development, and implementation of graphic, layout, and production communication materials.
                    </li>
                    <li>Delegate tasks to the 7 members of the design team and provide counsel on all aspects of the project.</li>
                    <li>Supervise the assessment of all graphic materials to ensure quality and accuracy.</li>
                    <li>Oversee the efficient use of production project budgets ranging from $2,000 - $25,000.</li>
                  </ul>
                </div>
  
                <div class="resume-item timeline-item">
                  <h4>Graphic Design Specialist</h4>
                  <h5>2017 - 2018</h5>
                  <p><em>Stepping Stone Advertising, New York, NY</em></p>
                  <ul>
                    <li>
                      Developed numerous marketing programs (logos, brochures, infographics, presentations, and advertisements).
                    </li>
                    <li>Managed up to 5 projects or tasks at a given time while under pressure.</li>
                    <li>Recommended and consulted with clients on the most appropriate graphic design.</li>
                    <li>Created 4+ design presentations and proposals a month for clients and account managers.</li>
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
  h2,h4,h5{
    font-family: "Fredoka", serif;
  }
  p{
  font-family: "Poppins", serif;
}
  .resume .resume-title {
    color: var(--heading-color);
    font-size: 26px;
    font-weight: 700;
    margin-top: 20px;
    margin-bottom: 20px;
  }
  .div{
    background-color: rgb(251, 217, 222);
  }
  /* Timeline Container */
  .timeline {
    position: relative;
    padding-left: 30px; /* Space for the timeline line */
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
  </style>
  