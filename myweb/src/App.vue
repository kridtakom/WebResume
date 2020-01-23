<template>
  <div id="app">
    <div id="colorlib-page">
      <a href="#" class="js-colorlib-nav-toggle colorlib-nav-toggle">
        <i></i>
      </a>
      <aside id="colorlib-aside" role="complementary" class="js-fullheight text-center">
        <h1 id="colorlib-logo">
          <a href="index.html">
            Kridtakom
            <span>.</span>
          </a>
        </h1>
        <nav id="colorlib-main-menu" role="navigation">
          <ul>
            <span style="color:#6f6c6c">
              <li>
                <i class="icon-phone"></i>
                Tel : 082858449
              </li>
              <li>
                <i class="icon-markunread_mailbox"></i> E-mail : kridtakom@gmail.com
              </li>
              <li>
                <i class="icon-my_location"></i>
                Address : 170 soi taksin 14/2 Taksin road Bukkalo Thonburi
                Bangkok 10600
              </li>
            </span>
            <li>
              <br />
            </li>
            <li>
              <a href="https://www.dropbox.com/s/o5d8rw4bdpe4liz/transcript-60130500004.pdf?raw=1">
                <i class="icon-paperclip"></i>&nbsp; Transcript
              </a>
            </li>
            <li>
              <a href="#">
                <i class="icon-person"></i>&nbsp;Resume
              </a>
            </li>
          </ul>
        </nav>

        <div class="colorlib-footer">
          <ul>
            <li>
              <a href="https://www.facebook.com/kridtakom.boom">
                <i class="icon-facebook"></i>
              </a>
            </li>
            <li>
              <a href="https://www.instagram.com/boommmmmmmmmmmmmmmmmmmmmmmmmmm/?hl=th">
                <i class="icon-instagram"></i>
              </a>
            </li>
            <li>
              <a href="https://github.com/kridtakom">
                <i class="icon-github"></i>
              </a>
            </li>
          </ul>
        </div>
      </aside>
      <!-- END COLORLIB-ASIDE -->
      <div id="colorlib-main">
        <div
          class="hero-wrap js-fullheight"
          :style="{'background-image': 'url(' + require('./assets/bg_1.jpg') + ')'}"
          data-stellar-background-ratio="0.5"
        >
          <div class="overlay"></div>
          <div class="js-fullheight d-flex justify-content-center align-items-center">
            <div class="col-md-8 text text-center">
              <div
                class="img mb-4"
                :style="{'background-image': 'url(' + require('./assets/IMG_4365-2.jpg') + ')'}"
              ></div>
              <div class="desc">
                <h2 class="subheading">Hello I'm</h2>
                <h1 class="mb-4">Kridtakom Chokanunvanit</h1>
                <p class="mb-4" style="color: #6f6c6c;">
                  I am a beginner Developer
                  <br />School of Information Technology, KMUTT
                </p>
              </div>
            </div>
          </div>
        </div>
        <section class="ftco-section">
          <div class="container">
            <div class="row justify-content-center mb-5 pb-2">
              <div class="col-md-7 heading-section text-center ftco-animate">
                <h2 class="mb-4">Projects and Works</h2>
                <p>
                  These are projects and works in Bachelor of Science
                  (Information Technology)
                </p>
              </div>
            </div>
            <div class="row">
              <div class="col-md-4" v-for="(project, index) in projects" :key="index">
                <div class="blog-entry ftco-animate">
                  <a
                    href="#"
                    class="img img-2"
                    :style="{ backgroundImage: 'url('+project.Image+')' }"
                  ></a>
                  <div class="text text-2 pt-2 mt-3">
                    <span class="category mb-3 d-block">
                      <a href="#">{{project.Course}}</a>
                    </span>
                    <h3 class="mb-4">
                      <a href="#">{{project.Name}}</a>
                    </h3>
                    <p class="mb-4">{{project.Description}}</p>
                    <div class="author mb-4 d-flex align-items-center">
                      <div class="info">
                        <span></span>
                        <h3>
                          <span>{{project.Year}}</span>
                        </h3>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
              <div class="col-md-4">
                <div class="blog-entry ftco-animate">
                  <a
                    href="#"
                    class="img img-2"
                    style="background-image: url(https://www.dropbox.com/s/ej2tugkaxa0jzvj/webtech.PNG?raw=1);"
                  ></a>

                  <div class="text text-2 pt-2 mt-3">
                    <span class="category mb-3 d-block">
                      <a href="#">Technology</a>
                    </span>
                    <h3 class="mb-4">
                      <a href="#">The Newest Technology On This Year 2019</a>
                    </h3>
                    <p class="mb-4">
                      Even the all-powerful Pointing has no control about the
                      blind texts it is an almostEven the all-powerful Pointing
                      has no control about the blind texts it is an almostEven
                      the all-powerful Pointing has no control about the blind
                      texts it is an almostEven the all-powerful Pointing has no
                      control about the blind texts it is an almostEven the
                      all-powerful Pointing has no control about the blind texts
                      it is an almostEven the all-powerful Pointing has no
                      control about the blind texts it is an almost
                    </p>
                    <div class="author mb-4 d-flex align-items-center">
                      <div class="info">
                        <span>Create in</span>
                        <h3>
                          <span>Year</span>
                        </h3>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </section>
      </div>
      <!-- END COLORLIB-MAIN -->
    </div>
    <!-- END COLORLIB-PAGE -->
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "app",
  components: {},
  data() {
    return {
      projects: []
    };
  },
  async mounted() {
    const urlProject =
      "https://script.google.com/macros/s/AKfycbynRlK1sysszgfiSj095HOfjF9yWIkEWQ_xunJfKyJw0qZD5EA2/exec?path=/product";
    await axios.get(urlProject).then(res => {
      this.projects = res.data.items;
    });
  },
  methods: {}
};
</script>

<style>
</style>
