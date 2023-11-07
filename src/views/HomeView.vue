<template>
  <!-- home -->

  <v-app id="home">
    <NavBar />
    <v-container fluid>
      <div class="head">
        <v-row>
          <v-col cols="5">
            <div style="position: relative" class="mt-16">
              <h1 class="text-grey">Hello,</h1>
              <h1 class="text-white">I'M Rishabh Vaishya</h1>
              <span class="text-grey">Web Developer</span><br />
              <v-btn title dark class="text-yellow mt-8" variant="outlined"
                >Contact me</v-btn
              >
            </div>
          </v-col>
          <v-col cols="2">
            <div
              style="
                position: absolute;
                z-index: 9999;
                bottom: 0;
                margin-left: auto;
                margin-right: auto;
                left: 0;
                right: 0;
                text-align: center;
              "
            >
              <v-icon>fas fa-angle-double-down</v-icon>
            </div>
          </v-col>
          <v-col cols="5">
            <div style="position: relative; z-index: 9999" class="mt-16">
              <v-img class="circular--square" src="rishabh.png"></v-img>
            </div>
          </v-col>
        </v-row>
      </div>

      <!-- about -->

      <v-col cols="12" class="mt-16" id="about">
        <div>
          <v-row>
            <v-col cols="12" sm="6">
              <div class="egg">
                <v-img src="kl.png" style="border-radius: 50%; max-height: 280px; max-width:330px; padding-bottom: 100px;"></v-img>
              </div>
            </v-col>
            <v-col cols="12" sm="6">
              <h5 class="mt-16">About Me</h5>
              <div style="width: 120px">
                <v-slider v-model="slider2" color="yellow" label=""> </v-slider>
              </div>
              <h4 class="mt-n4">I am a Creative Web Design</h4>
              <h4>And Developer</h4>
              <p class="text-grey">
                Being a hardworking, sincere, positive ,and motivated person, to
                persue a carrer in the software industry as an efficient and
                dependable employee and to be a part of a progressive
                organizations that gives a scope to enhance my knowledge and
                skills.
              </p>
              <br />
              <p class="text-grey">
                I am an enthusiastic, self-motivated, reliable, responsible and
                hard working person. I am a mature team worker and adaptable to
                all challenging situations. I am able to work well both in a
                team environment as well as using own initiative. I am able to
                work well under pressure and adhere to strict deadlines.
              </p>
              <br />
              <p class="text-grey">
                To secure a position as an engineer in a company that
                specializes in the development of clean energy technologies.
              </p>
              <div id="app">
                <v-btn @click="onClick" title dark color="yellow" class="mt-4">
                  Download Resume
                </v-btn>
              </div>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <div class="text-center mt-4">
        <h2>What we Do</h2>
        <div style="width: 120px; margin: 0 auto">
          <v-slider v-model="slider2" color="yellow" label=""></v-slider>
        </div>
      </div>

      <!-- portfolio -->

      <v-col cols="12" class="padd" id="portfolio">
        <div class="first" id="project">
          <v-row>
            <v-col cols="12">
              <div class="child">
                <v-btn
                  icon="fas fa-laptop"
                  color="#FBDF7E"
                  class="text-white"
                ></v-btn>
                <h3 class="ml-3 mt-4">Web Design</h3>
                <p class="text-grey ml-3 text-caption">
                  the process of planning, conceptualizing,<br />
                  and implementing the plan for designing a website<br />
                  in a way that is functional and<br />
                  offers a good user experience.
                </p>
              </div>
              <div class="child">
                <v-btn
                  icon="fas fa-mobile-alt"
                  color="#FBDF7E"
                  class="text-white"
                ></v-btn>
                <h3 class="ml-3 mt-4">Android Developer</h3>
                <p class="text-grey ml-3 text-caption">
                  Web developers create functional,<br />
                  user-friendly websites and<br />
                  web applications.
                </p>
              </div>
              <div class="child">
                <v-btn
                  icon="fas fa-laptop"
                  color="#FBDF7E"
                  class="text-white"
                ></v-btn>
                <h3 class="ml-3 mt-4">App design</h3>
                <p class="text-grey ml-3 text-caption">
                  App design is an ongoing process <br />of creating user
                  experience (UX)<br />
                  and user interface (UI) elements for your application.
                </p>
              </div>
            </v-col>
          </v-row>
          <v-divider color="black"></v-divider>
        </div>
      </v-col>

      <!-- services -->

      <v-col cols="12" sm="12" id="services">
        <div class="d-flex justify-center mb-6">
          <v-btn color="#FBDF7E" class="mr-2">All</v-btn>
          <v-btn class="mr-2" variant="tonal">Web design</v-btn>
          <v-btn class="mr-2" variant="tonal">Front Design</v-btn>
          <v-btn class="mr-2" variant="tonal">Photography</v-btn>
          <v-btn variant="tonal">Illustration</v-btn>
        </div>
      </v-col>
      <v-col cols="12" class="imgHover">
        <v-row class="fill-height" align="center" justify="center">
          <template v-for="(item, i) in items" :key="i">
            <v-col cols="12" md="4">
              <v-hover v-slot="{ isHovering, props }">
                <v-card
                  :elevation="isHovering ? 12 : 2"
                  :class="{ 'on-hover': isHovering }"
                  v-bind="props"
                >
                  <v-img src="androiddd.jpg" height="225px" cover></v-img>
                </v-card>
              </v-hover>
            </v-col>
          </template>
        </v-row>
      </v-col>
      <v-col cols="12" sm="12">
        <div class="d-flex justify-center mb-6">
          <v-btn color="#FBDF7E" class="mt-4">Load More</v-btn>
        </div>
      </v-col>

      <!-- Page -->

      <v-col cols="12" id="page">
        <div class="pre">
          <v-row>
            <v-col cols="12" sm="4">
              <v-card class="mw-auto" max-width="344" height="">
                <v-img src="backend.jpg" height="200px" cover></v-img>
                <v-card-title>We provide you the best..!</v-card-title>
                <v-card-subtitle> By Rishabh | 06 sep 2023 </v-card-subtitle>
                <v-card-text> Backend Developer Skills </v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" sm="4">
              <v-card class="mw-auto" max-width="344" height="">
                <v-img src="fronted.png" height="200px" cover></v-img>
                <v-card-title>We provide you the best..!</v-card-title>
                <v-card-subtitle> By Rishabh | 06 sep 2023 </v-card-subtitle>
                <v-card-text> Frontend Developer Skills </v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" sm="4">
              <v-card class="mw-auto" max-width="344" height="">
                <v-img src="androidd.jpg" height="200px" cover></v-img>
                <v-card-title>We provide you the best..!</v-card-title>
                <v-card-subtitle> By Rishabh | 06 sep 2023 </v-card-subtitle>
                <v-card-text> Android Developer skills </v-card-text>
              </v-card>
            </v-col>
          </v-row>
        </div>
      </v-col>

      <!-- Biog -->

      <v-col cols="12" id="biog">
        <div class="hire">
          <v-row>
            <v-col cols="12" sm="8">
              <h1 class="mt-9">Hire me for your awesome project</h1>
              <p class="text-grey">I will try to give you the best..!</p>
            </v-col>
            <v-col cols="12" sm="4">
              <v-btn color="#FBDF7E" class="mt-15">Hire Me</v-btn>
            </v-col>
          </v-row>
        </div>
      </v-col>

      <!-- contact -->

      <v-col cols="12" sm="12" class="px-16" id="contact">
        <v-row>
          <v-col cols="12" sm="4">
            <div class="child">
              <h1>Contact Info</h1>
              <v-btn
                icon="fas fa-map-marker-alt"
                class="mt-10"
                variant="outlined"
              ></v-btn
              ><br />
              <span class="text-caption">Your Street SYO, your Area Dream</span
              ><br />
              <v-btn
                icon="fas fa-phone-alt"
                class="mt-10"
                variant="outlined"
              ></v-btn
              ><br />
              <span class="text-caption">8707252061</span><br />
              <span class="text-caption">9554100605</span><br />
              <v-btn
                icon="fas fa-envelope"
                class="mt-10"
                variant="outlined"
              ></v-btn
              ><br />
              <span class="text-caption">rishabhvaishya7@gmail.com</span><br />
              <span class="text-caption"
                >rishabh.vaishaya20@smslucknow.ac.in</span
              ><br />
            </div>
          </v-col>
          <v-col cols="12" sm="8">
            <h1 class="mt-8">Send your message</h1>
            <v-divider></v-divider>
            <span class="text-caption">
              If u like my Portfolio then you can...!
            </span>
            <v-row class="mt-10">
              <v-col cols="12" sm="6">
                <v-text-field
                  label="Name"
                  persistent-hint
                  variant="outlined"
                ></v-text-field>
              </v-col>
              <v-col cols="12" sm="6">
                <v-text-field
                  label="Phone No"
                  persistent-hint
                  variant="outlined"
                ></v-text-field>
              </v-col>
            </v-row>
            <v-textarea
              label="Message"
              persistent-hint
              variant="outlined"
            ></v-textarea>
            <v-btn color="#FBDF7E" class="mt-2">Submit Now</v-btn>
          </v-col>
        </v-row>
      </v-col>
    </v-container>

    <!-- FooterView -->

    <FooterView />
  </v-app>
</template>


<!-- scripttag -->

<script>
//components

import NavBar from "@/components/NavBar.vue";
import FooterView from "@/components/FooterView.vue";

import { defineComponent } from "vue"; // Import Vue 3's defineComponent

export default defineComponent({
  name: "HomeView",
  setup() {
    
    const onClick = () => {
      // Perform validation checks here

      downloadResume();

      // Validation failed, show an error message or take appropriate action
      //showError();
    };

    const downloadResume = () => {
      // Logic to initiate the download action when validation passes
      // Replace with your download logic
      // For example, you can create a link to the file and trigger a click event
      const downloadLink = document.createElement("a");
      downloadLink.href = "/cvrishabh.pdf"; // Replace with the actual file path
      downloadLink.download = "cvrishabh.pdf"; // Specify the file name
      downloadLink.click();
    };

    // const showError = () => {
    //   // Your code to handle validation errors (e.g., show an error message)
    //   alert("Validation failed. Please try again.");
    // };

    return {
      onClick,
      slider2: 50,
      items: [
        {
          img: "",
        },
        {
          img: "",
        },
        {
          img: "",
        },
        {
          img: "",
        },
        {
          img: "",
        },
        {
          img: "",
        },
      ],
    };
  },
  components: {
    NavBar,
    FooterView,
  },
});
</script>


<!-- styleview -->

<style scoped>
.circular--square {
  border-radius: 50%;
  height: 300px;
  width: 400px;
}

.v-container {
  padding: 16px 0;
}
.head {
  position: relative;
  text-align: center;
  padding: 12px;
  margin-bottom: 6px;
  height: 400px;
  width: 100%;
  color: white;
}
.head:before {
  content: " ";
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, 6deg);
}
.head:after {
  content: " ";
  position: absolute;
  top: 0;
  right: 0;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, -6deg);
}
.egg {
  display: block;
  margin-left: 100px;
  margin-top: 50px;
  width: 356px;
  height: 300px;
  background-color: #fbdf7e;
  border-radius: 50% 50% 50% 50% / 60% 60% 40% 0%;
}
.first {
  width: 100%;
  height: 200%;
  text-align: center;
  padding: 2rem 1rem;
}
.child {
  display: inline-block;
  padding: 2rem 1rem;
  vertical-align: middle;
  text-align: center;
  margin-right: 8px;
}
.imgHover {
  padding: 0 200px;
}
.pre {
  width: 100%;
  height: 380px;
  text-align: center;
  padding: 0 200px;
  background-color: #f5f5f5;
}
.hire {
  width: 100%;
  height: 200px;
  padding: 0 200px;
  background-color: #e9e9e9;
  margin-top: -24px;
}
</style>
