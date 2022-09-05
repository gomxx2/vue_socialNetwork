<template>
  <header class="header-area">
    <!-- <top-bar /> -->
    <div class="header-centerbar">
      <div class="container">
        <div class="row align-items-center">
          <div class="col-lg-4">
            <div class="logo">
              <router-link to="/">
                <h1>SocialNetwork</h1>

                <!-- <img :src="require(`@/assets/images/` + image)" alt="feature" /> -->
              </router-link>
            </div>
          </div>
          <div class="col-lg-8">
            <div class="header-centerbar-ad">
              <div class="header-menu-search">
                <div class="input-group mb-2 mr-sm-2">
                  <input type="text" class="form-control" id="inlineFormInputGroupUsername2" placeholder="Username">
                  <div class="input-group-prepend">
                    <div class="input-group-text">                     
                        <a href="#"><i class="fal fa-search"></i></a>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="header-menubar">
      <div class="container">
        <div class="row align-items-right">
          <div class="col-lg-12 col-sm-35 col-3">
            
            <nav-items :darkClass="darkClass" />
          </div>
       
        </div>
      </div>
    </div>
  </header>
</template>

<script>
// import TopBar from "./TopBar.vue";
import NavItems from "../Common/NavItems.vue";
export default {
  components: { 
    // TopBar
    NavItems },
  props: {
    image: {
      type: String,
      default: "logo.png",
    },
    darkClass: {
      type: Object,
    },
  },
  data: () => ({
    value: null,
    options: ["English", "Bangla", "Hinde"],
  }),
  methods: {
    hideSidebar(e) {
      this.$emit("toggleSidebar", e);
    },
  },
};
</script>
<style>
.select-lang {
  border: 1px solid #bababa;
  width: 100px;
  padding: 2px;
  color: #17191d;
  outline: none;
  border-radius: 7px;
}
</style>
