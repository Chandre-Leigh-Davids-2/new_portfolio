<template>
  <div>
    <header id="header" class="header d-flex flex-column justify-content-center">
      <i class="header-toggle d-xl-none bi bi-list"></i>

      <nav id="navmenu" class="navmenu">
        <ul>
          <li><a href="#hero" class="active"><i class="bi bi-house navicon"></i><span>Home</span></a></li>
          <li><a href="#about"><i class="bi bi-person navicon"></i><span>About</span></a></li>
          <li><a href="#resume"><i class="bi bi-file-earmark-text navicon"></i><span>Resume</span></a></li>
          <li><a href="#portfolio"><i class="bi bi-images navicon"></i><span>Portfolio</span></a></li>
          <li><a href="#contact"><i class="bi bi-envelope navicon"></i><span>Contact</span></a></li>
        </ul>
      </nav>
    </header>
  </div>
</template>

<script>
export default {
  mounted() {
    this.$nextTick(() => {
      this.initHeaderToggle();
      this.initNavmenuScrollspy();
      this.initScrollTopButton();
      this.initMobileNavClose();
    });
  },
  beforeDestroy() {
    window.removeEventListener('load', this.navmenuScrollspy);
    document.removeEventListener('scroll', this.navmenuScrollspy);
    document.removeEventListener('scroll', this.toggleScrollTop);
  },
  methods: {
    initHeaderToggle() {
      const headerToggleBtn = document.querySelector('.header-toggle');
      const headerToggle = () => {
        document.querySelector('#header').classList.toggle('header-show');
        headerToggleBtn.classList.toggle('bi-list');
        headerToggleBtn.classList.toggle('bi-x');
      };
      headerToggleBtn.addEventListener('click', headerToggle);
    },

    initNavmenuScrollspy() {
      const navmenulinks = document.querySelectorAll('.navmenu a');
      const navmenuScrollspy = () => {
        navmenulinks.forEach(navmenulink => {
          if (!navmenulink.hash) return;
          let section = document.querySelector(navmenulink.hash);
          if (!section) return;
          let position = window.scrollY + 200;
          if (position >= section.offsetTop && position <= (section.offsetTop + section.offsetHeight)) {
            document.querySelectorAll('.navmenu a.active').forEach(link => link.classList.remove('active'));
            navmenulink.classList.add('active');
          } else {
            navmenulink.classList.remove('active');
          }
        });
      };
      window.addEventListener('load', navmenuScrollspy);
      document.addEventListener('scroll', navmenuScrollspy);
    },

    initScrollTopButton() {
      let scrollTop = document.querySelector('.scroll-top');
      const toggleScrollTop = () => {
        if (scrollTop) {
          window.scrollY > 100 ? scrollTop.classList.add('active') : scrollTop.classList.remove('active');
        }
      };
      scrollTop.addEventListener('click', (e) => {
        e.preventDefault();
        window.scrollTo({
          top: 0,
          behavior: 'smooth'
        });
      });
      window.addEventListener('load', toggleScrollTop);
      document.addEventListener('scroll', toggleScrollTop);
    },

    initMobileNavClose() {
      document.querySelectorAll('#navmenu a').forEach(navmenu => {
        navmenu.addEventListener('click', () => {
          if (document.querySelector('.header-show')) {
            document.querySelector('.header-toggle').click(); // Closes the nav
          }
        });
      });
    }
  }
};
</script>

<style scoped>
.header {
  color: var(--default-color);
  position: fixed;
  top: 0;
  left: 0;
  bottom: 0;
  padding: 0 15px;
  transition: all ease-in-out 0.3s;
  overflow-y: auto;
  z-index: 997;
  min-width: 200px;
}

@media (max-width: 1199px) {
  .header {
    background-color: var(--background-color);
    border-right: 1px solid color-mix(in srgb, var(--default-color), transparent 90%);
    width: 300px;
    left: -100%;
  }
}

@media (min-width: 1200px) and (max-width: 1600px) {
  .header~main {
    margin-left: 160px;
  }

  .header~main .hero {
    margin-left: -160px;
    width: 100vw;
  }
}

.header.header-show {
  left: 0;
}

.header .header-toggle {
  color: var(--contrast-color);
  background-color: var(--accent-color);
  font-size: 22px;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  cursor: pointer;
  position: fixed;
  top: 15px;
  right: 15px;
  z-index: 9999;
  transition: background-color 0.3s;
}

.header .header-toggle:hover {
  color: var(--contrast-color);
  background-color: color-mix(in srgb, var(--accent-color) 90%, white 15%);
}
.navmenu {
  padding: 0;
  z-index: 9997;
}

.navmenu ul {
  list-style: none;
  padding: 0 0 20px 0;
  margin: 0;
  width: 140px;
}

.navmenu a,
.navmenu a:focus {
  color: white;
  display: flex;
  align-items: center;
  padding: 10px 18px;
  margin-bottom: 8px;
  font-size: 15px;
  border-radius: 50px;
  background: pink;
  border: 1px solid pink;
  height: 56px;
  width: 100%;
  overflow: hidden;
  transition: 0.3s;
}

.navmenu a i,
.navmenu a:focus i {
  font-size: 20px;
}

.navmenu a span,
.navmenu a:focus span {
  padding: 0 5px 0 7px;
}

@media (min-width: 992px) {

  .navmenu a,
  .navmenu a:focus {
    max-width: 56px;
  }

  .navmenu a span,
  .navmenu a:focus span {
    display: none;
  }
}

.navmenu a:hover,
.navmenu .active,
.navmenu .active:focus,
.navmenu li:hover>a {
  color: pink;
  background:white ;
  border: 1px solid pink;
}

.navmenu a:hover,
.navmenu li:hover>a {
  max-width: 100%;
  color: pink;
  background:white ;
  border: 1px solid pink;
}

.navmenu a:hover span,
.navmenu li:hover>a span {
  display: block;
}
</style>
