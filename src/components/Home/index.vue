<template>
  <div>
    <video-pop-up />
    <drawer @toggleSidebar="toggleSidebar" :sidebar="sidebar" />
    <!--====== HEADER PART START ======-->
    <header-one image="logo.png" @toggleSidebar="toggleSidebar" />
    <!--====== HEADER PART ENDS ======-->

    <!--====== POST PART START ======-->

    <!-- <post-part-home-one /> -->

    <!--====== POST PART ENDS ======-->

    <!--====== POST GALLERY PART START ======-->
    <post-gallery />

    <!--====== POST GALLERY PART ENDS ======-->

    <!--====== FEATURE PART START ======-->
   

    <!--====== VIDEO NEWS PART ENDS ======-->

    <!--====== ALL POST PART START ======-->

    <section class="all-post-area">
      <div class="container">
        <div class="row justify-content-center">
          <div class="col-lg-8">
          
         
            <div class="post-add mt-30">
              <a href="#"
                ><img src="@/assets/images/ads/one_ad.png" alt="ad"
              /></a>
            </div>
           
          </div>
          <div class="col-lg-4">
            <div class="all-post-sidebar">
              <share-post />
              <div class="upcoming-matches-post mt-35">
                <div
                  class="
                    section-title
                    d-flex
                    justify-content-between
                    align-items-center
                  "
                >
                  <h3 class="title">Upcoming Matches</h3>
                  <a href="#">ALL SEE</a>
                </div>
               
              </div>
            
              <div class="Categories-post mt-40">
                <div
                  class="
                    section-title
                    d-flex
                    justify-content-between
                    align-items-center
                  "
                >
                  <h3 class="title">Categories</h3>
                  <a href="#">ALL SEE</a>
                </div>

              
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!--====== ALL POST PART ENDS ======-->

    <!--====== FOOTER PART START ======-->
    <footer-one />

    <!--====== FOOTER PART ENDS ======-->

    <!--====== GO TO TOP PART START ======-->
    <div class="go-top-area">
      <div class="go-top-wrap">
        <div class="go-top-btn-wrap">
          <a href="#" class="go-top go-top-btn d-block">
            <i class="fa fa-angle-double-up"></i>
            <i class="fa fa-angle-double-up"></i>
          </a>
        </div>
      </div>
    </div>
    <!--====== GO TO TOP PART ENDS ======-->
  </div>
</template>
<script>
import HeaderOne from "../Utility/Header/index";
// import PostPartHomeOne from "./PostPartHomeOne.vue";
import PostGallery from "./PostGallery.vue";


import SharePost from "./SharePost.vue";
import FooterOne from "../Utility/Footer/FooterOne.vue";
import Drawer from "../Mobile/Drawer.vue";
import VideoPopUp from "../Utility/VideoPopUp.vue";
export default {
  components: {
    HeaderOne,
    // PostPartHomeOne,
    PostGallery,
  
    SharePost,
    FooterOne,
    Drawer,
    VideoPopUp,
  },
  data: () => ({
    sidebar: false,
  }),
  created() {
    document.addEventListener("scroll", this.topToBottom);
  },
  methods: {
    toggleSidebar() {
      this.sidebar = !this.sidebar;
    },
    topToBottom() {
      const result = document.querySelector(".go-top");
      if (
        document.body.scrollTop > window.innerHeight ||
        document.documentElement.scrollTop > window.innerHeight
      ) {
        result.classList.add("active");
      } else {
        result.classList.remove("active");
      }
    },
  },
};
</script>

<style scoped>
/* play post */
.single-play-post-area .single-play-box {
  padding: 23px 12px !important;
}
</style>
