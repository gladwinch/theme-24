<template>
<v-app>
  <!-- Header -->

  <div class="header-cont d-flex align-center mb-6">
      <div class="d-flex header-left">
        <div class="ct-block-1 d-flex justify-end align-end">
          <div class="ct-block-2 hidden-md-and-down">
             <div class="ct-block-3 pa-2">
                <img src="./assets/earth.png" alt="world" class="world-img " >
                <v-avatar class="ct-avatar" height="100" width="100">
                  <img src="./assets/profileimg.png" alt="profilepic" class="profile-pic">
                </v-avatar>

                <v-avatar class="ct-msg-icon" height="20" width="20">
                   <img src="./assets/msg.png" alt="msgpic" class="profile-pic">
                </v-avatar>
             </div>
          </div>
        </div>

        
      </div>
      
      <v-container class="d-flex align-center">
        <div class="make-space hidden-md-and-down"></div>
        <div class="header-info">
          <div class="subtitle-1 font-weight-bold white--text mb-1">Tanbir Ahemd</div>
          <div class="caption white--text mb-2 ct-btn-icon">
            User Interface Designer
          </div>
          <div class="mt-2 ct-icon-list ct-postion">
            <img src="./assets/icons/twitter.png" alt="twitter" class="ct-icon mr-4" >
            <img src="./assets/icons/instagram.png" alt="instagram" class="ct-icon mr-4" >
            <img src="./assets/icons/linkedin.png" alt="linkedin" class="ct-icon" >
          </div>
        </div>

        <v-spacer></v-spacer>

        <div class="header-right d-flex align-center">

           <div class="d-flex align-center mr-6">
             <img src="./assets/icons/audio.png" alt="audio" class="ct-icon hidden-sm-and-down" >
              <div class="caption ml-4 white--text hidden-sm-and-down">Audio & Text</div>
           </div>

           <div class="d-flex align-center mr-6">
             <img src="./assets/icons/video.png" alt="video" class="ct-icon hidden-sm-and-down" >
              <div class="caption ml-4 white--text hidden-sm-and-down">Play Video</div>
           </div>

           <div class="text-center mr-6">
             <div class="font-weight-bold white--text hidden-sm-and-down">$15</div>
             <div class="white--text body-2 hidden-sm-and-down">Hourly rate</div>
           </div>

           <div class="text-center mr-6">
             <div class="font-weight-bold white--text hidden-sm-and-down">10 hours</div>
             <div class="white--text body-2 hidden-sm-and-down">Weekly Availability</div>
           </div>

        </div>
        <v-btn 
              color="#6884F3" 
              depressed 
              rounded 
              class="text-capitalize white--text">
                Hire me
            </v-btn>
      </v-container>

  </div>

  <!-- Header end -->

  <!-- Tabs start -->

  <v-container class="mt-12">
    <v-tabs
      grow
      center-active
      rounded
      hide-slider
    >
      <v-tab
        v-for="tab in tabs"
        :key="tab.id"
        @click="currentTab = tab.id"
        class="ct-tab-title text-capitalize"
        :class="[
          currentTab == tab.id ? 'active-tab' : '', 'ct-tab',
          tab.id == 1 ? 'round-left' : '',
          tab.id == 4 ? 'round-right' : '',
          tab.id != 4 ? 'mr-xs-2 mr-md-12' : ''
        ]"
      >
        <v-avatar tile height="20" width="23">
        <img :src="getImgUrlIcon(currentTab == tab.id ? tab.image + '1': tab.image)" class="mr-4">
        </v-avatar>
        {{ tab.title }}
      </v-tab>
    </v-tabs>

  <!-- Tabs end -->

  <!-- Tab content 1 start -->

    <div class="content mt-12">
      <div v-if="currentTab == 1" class="primary--text">
          <v-tabs
            centered
            color="#4E6EF1"
            class="ct-sec-tab"
          >
            <v-tab class="text-capitalize">All</v-tab>
            <v-tab class="text-capitalize">Web Design</v-tab>
            <v-tab class="text-capitalize">Resume</v-tab>
            <v-tab class="text-capitalize">UX Design</v-tab>
            <v-tab class="text-capitalize">Animation</v-tab>
          </v-tabs>

          <v-row class="mt-10">
            <v-col
              v-for="n in 6"
              :key="n"
              cols="12"
              sm="6"
              md="4"
            >
               <v-img :src="getImgUrl(n)" 
                  max-height="300" max-width="340" 
                  min-height="270" min-width="270" 
                  aspect-ratio="1" class="ct-image mx-auto"></v-img>
            </v-col>
          </v-row>
      </div>

    <!-- Tab content 1 end -->

    <!-- Tab content 2 start -->

      <div v-if="currentTab == 2">
        <div class="subtitle-2">Work Experince</div>
        <v-divider></v-divider>

        <div class="mt-10">
          <div class="d-flex">
            <div class="mr-12 caption">May 2017 - June 2018</div>
            <div class="ct-bar mr-12">
               <div class="ct-circle"></div>
               <div class="ct-circle mt-5"></div>
            </div>
            <div class="right-panel">
              <div class="title pt-0">Staff Asia Sylhet</div>
              <div class="ct-caption">Web Designer</div>
              <p class="caption pt-4">Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores.Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod labore et dolore magna aliquyam erat.</p>
            </div>
          </div>

          <div class="d-flex">
            <div class="mr-12 caption">May 2017 - June 2018</div>
            <div class="ct-bar mr-12">
               <div class="ct-circle"></div>
               <div class="ct-circle mt-5"></div>
            </div>
            <div class="right-panel">
              <div class="title">Staff Asia Sylhet</div>
              <div class="ct-caption">Web Designer</div>
              <p class="caption pt-4">Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores.Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod labore et dolore magna aliquyam erat.</p>
            </div>
          </div>

          <div class="d-flex">
            <div class="mr-12 caption">May 2017 - June 2018</div>
            <div class="ct-bar mr-12">
               <div class="ct-circle"></div>
               <div class="ct-circle mt-5"></div>
            </div>
            <div class="right-panel">
              <div class="title">Staff Asia Sylhet</div>
              <div class="ct-caption">Web Designer</div>
              <p class="caption pt-4">Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores.Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod labore et dolore magna aliquyam erat.</p>
            </div>
          </div>
        </div>
      </div>

    <!-- Tab content 2 end -->

    <!-- Tab content 3 start -->

      <div v-if="currentTab == 3">
        <div class="subtitle-2">Educational Qualifications</div>
        <v-divider></v-divider>

        <div class="mt-10">
          <div class="d-flex">
            <div class="mr-12 caption">May 2017 - June 2018</div>
            <div class="ct-bar mr-12">
               <div class="ct-circle"></div>
               <div class="ct-circle mt-5"></div>
            </div>
            <div class="right-panel">
              <div class="title pt-0">Sylhet Ideal College</div>
              <div class="ct-caption">Higher Secondary Certificate</div>
              <p class="caption pt-4">Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores.Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod labore et dolore magna aliquyam erat.</p>
            </div>
          </div>

          <div class="d-flex">
            <div class="mr-12 caption">May 2017 - June 2018</div>
            <div class="ct-bar mr-12">
               <div class="ct-circle"></div>
               <div class="ct-circle mt-5"></div>
            </div>
            <div class="right-panel">
              <div class="title">Modanmohon College</div>
              <div class="ct-caption">Bachelor Degree of Computer Science</div>
              <p class="caption pt-4">Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores.Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod labore et dolore magna aliquyam erat.</p>
            </div>
          </div>

          <div class="d-flex">
            <div class="mr-12 caption">May 2017 - June 2018</div>
            <div class="ct-bar mr-12">
               <div class="ct-circle"></div>
               <div class="ct-circle mt-5"></div>
            </div>
            <div class="right-panel">
              <div class="title">Leading University</div>
              <div class="ct-caption">Leading University</div>
              <p class="caption pt-4">Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores.Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod labore et dolore magna aliquyam erat.</p>
            </div>
          </div>
        </div>
      </div>

    <!-- Tab content 3 end -->

    <!-- Tab content 4 start -->

      <div v-if="currentTab == 4">
        <div>
          <div class="subtitle-2">Design Skills</div>
          <v-divider></v-divider>
          <div class="d-flex mt-12">
            <div>100%</div>
            <div class="bar-cont ml-10 d-flex align-end light-it" v-for="skill in skills" :key="skill.id">
              <div>
                <div :style="{ height: skill.value/5.8 + 'rem', width: '20rem' }" class="primary pt-2 progress text-center">{{ skill.value }}%</div>
                <div class="text-center caption white black--text pt-2">{{ skill.skill }}</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Tab content 4 end -->

  </v-container>
</v-app>
</template>

<script>
  export default {
    data () {
      return {
        currentTab: 1,
        tabs: [
          { title: 'Portfolio', id: 1, image: 'layer' }, 
          { title: 'Works', id: 2, image: 'portfolio' },
          { title: 'Education', id: 3, image: 'book' }, 
          { title: 'Design Skill', id: 4, image: 'idea' }
        ],
        skills: [
          { skill: "PS", value: 80, id: 1 },
          { skill: "Al", value: 35, id: 2 },
          { skill: "XD", value: 92, id: 3 },
          { skill: "UI", value: 55, id: 4 },
          { skill: "UX", value: 72, id: 5 }
        ]
      }
    },

    methods: {
        getImgUrl(id) {
           let image = require.context('./assets/portfolio', false, /\.png$/)
           return image('./' + id + ".png")
        },
        getImgUrlIcon(icon) {
           let image = require.context('./assets/icons/tabs', false, /\.png$/)
           return image('./' + icon + ".png")
        }
    }
  }
</script>

<style>
/* Global style */
.primary { background-color: #4E6EF1 !important; }
.primary--text { color: #4E6EF1 !important; }
.light-it  { background-color:rgb(229, 229, 231) !important; }
.light-it--text { color: rgb(233, 233, 236) !important; }
/* Global style end*/

/* Header styles */

.header-cont {
  background-color: #4E6EF1;
  height: 8rem;
  width: 100%;
  position: relative;
  z-index: 1;
}

.make-space {
  width: 20%;
  height: 1px;
}

.header-left {
  /* background-color: #375AE8; */
  position: absolute;
  height: 12.5rem;
  width: 18rem;
}

.header-right--image {
  height: 9rem;
}

/* polygon shape */
.ct-block-1 {
  clip-path: polygon(100% 0, 100% 82%, 84% 100%, 0 100%, 0 0);
  height: 100%;
  width: 100%;
}

.ct-block-2 {
  height: 100%;
  width: 100%;
  background-color: #294DDF !important;
  clip-path: polygon(100% 0, 83.4% 82%, 100% 81.8%, 79.3% 100%, 0 100%, 0 0);
}

.ct-block-3 {
  height: 100%;
  width: 100%;
  background-color: #375AE8 !important;
  clip-path: polygon(99% 20%, 83% 84%, 79% 100%, 0 100%, 0 0);
}

/* inside polygon */
.world-img {
  height: 8rem;
  width: 14rem;
  margin-top: 3rem;
}

.ct-avatar {
  transform: translateX(7rem) translateY(-8rem);
  padding: 8px;
  background-color: white;
}

.ct-msg-icon {
  transform: translateX(4.8rem) translateY(-6rem);
}

/* polygon shape end */

/* icons style */
.ct-icon-list {
  transform: translateY(0.2rem)
}

.ct-icon {
  height: 2rem;
  width: 2rem;
}

/* .ct-postion {
  transform: translateX(-1rem) translateY(0.9rem);
}

.ct-btn-icon {
  transform: translateX(-0.5rem)
} */



/* Header styles end*/

/* Tab styles */

.ct-tab {
  background-color: rgb(233, 233, 233);
  color: rgb(87, 86, 86)!important;
  transition: 0.2s;
}

.ct-tab-title {
  font-size: 1.2rem !important;
  font-weight: 400 !important;
}

.active-tab {
  background-color: #4E6EF1;
  color: white!important
}


/* Corners */
.round-left {
  border-top-left-radius: 4rem;
  border-bottom-left-radius: 4rem;
}

.round-right {
  border-top-right-radius: 4rem;
   border-bottom-right-radius: 4rem;
}

/* Tab styles end*/

/* Contents style */

/* Content 1 style */

.ct-sec-tab {
  border-bottom: solid 1px rgb(184, 184, 184);

}

.ct-image {
  border-top-right-radius: 2rem;
  border-bottom-left-radius: 2rem;
}

/* Content 1 style end */

/* Content 2 style */

.ct-bar {
  height: 10rem;
  width: 0.1rem;
  background-color: #4E6EF1;
}

.ct-circle {
  height: 0.6rem;
  width: 0.6rem;
  border-radius: 1rem;
  background-color: #4E6EF1;
  transform: translateX(-4px)
}

.ct-caption {
  font-size: 0.8rem;
  color: grey;
  font-weight: 300;
}

.right-panel {
  max-width: 30rem;
  transform: translateY(-8px)
}

/* Design skill style */
.bar-cont {
  height: 20rem;
  width: 1.5rem;
}

.progress {
  width: 1.5rem !important;
  font-size: 0.6rem;
  color: white;
}

.ct-space {
  width: 4.85rem;
}

</style>