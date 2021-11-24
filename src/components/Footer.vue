<template>
  <footer>

    <!-- Section Newsletter -->
    <section class="_section-newsletter _p-medium">
      <div class="container">
        <h3>Subscribe to our Newsletter</h3>
        <div class="row justify-content-center">
          <div class="col-8">
          <input type="email" placeholder="Insert your email*" class="float-start">
          <a href="#" class="_btn-large _btn-black float-end">SEND</a>
          </div>  
        </div>
      </div>
    </section>

    <!-- Section Link -->
    <section class="_p-small">
      <div class="container">

        <div class="row gx-5">
          <div class="col-3 _section-link">
            <ul>
              <li><h4>AVADA TECH FORUM</h4></li>
              <li><h5>Sed semper, nisl id feugiat eleifend, erat est digssim felis, quis auctor elit enim nec ante. Cras et nibh risus. Pellentesque non mi sit amet mi intermentum.</h5></li>
            </ul>
          </div>

          <div class="col-3 _section-link _section-link-print" v-for="(link, i) in footerLink" :key="'link-'+ i">
            <ul>
              <li><h4> {{link.title}} </h4></li>
              <li class="_link pt-0"><p><i class="fa fa-angle-right" aria-hidden="true"></i>{{link.text1}}</p></li>
              <li class="_link"><p><i class="fa fa-angle-right" aria-hidden="true"></i>{{link.text2}}</p></li>
              <li class="_link"><p><i class="fa fa-angle-right" aria-hidden="true"></i>{{link.text3}}</p></li>
              <li class="_link"><p><i class="fa fa-angle-right" aria-hidden="true"></i>{{link.text4}}</p></li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- Section Social -->
    <section class="_section-social">
      <div class="container">

        <div class="d-flex justify-content-between align-items-center">
          <h5><i class="fa fa-copyright" aria-hidden="true"></i> Copyright 2012 - 2020 | Avada Theme by <span>Theme Fusion</span> | All Rights Reserved | Powered by <span>WordPress</span></h5>
          
          <div class="_icon-social">
            <a href="#" v-for="(social, i) in iconSocial" :key="'iconSocial-'+ i" :style="social.bgColor">
              <i :class="social.icon" aria-hidden="true" ></i>
            </a>
          </div>
        </div>

      </div>

      <a href="#" class="_btn-up-site"><i class="fa fa-angle-up" aria-hidden="true"></i></a>
    </section>

  </footer>
</template>

<script>
export default {
  name: 'Footer',
    data(){
    return{
      iconSocial: [
        {
          icon: "fa fa-facebook",
          bgColor: "background-color: #3c5998",
        },
        {
          icon: "fa fa-twitter",
          bgColor: "background-color: #54acee",
        },
        {
          icon: "fa fa-instagram",
          bgColor: "background-color: #3f729b",
        },
        {
          icon: "fa fa-youtube-play",
          bgColor: "background-color: #cd201f",
        },
      ],
      footerLink: [
        {
          title: "POPULAR TOPICS",
          text1: "Nam a dolor volutpat massa auctor semper",
          text2: "Sed euismod nunc urna fermentum arcu dapibus fringilla",
          text3: "Cras lacinia tellus id mauris finibus lacus molestie",
          text4: "Curabitur a scelerisque ligula",
        },
        {
          title: "RECENT TOPICS",
          text1: "Nam a dolor volutpat massa auctor semper",
          text2: "Sed euismod nunc urna fermentum arcu dapibus fringilla",
          text3: "Cras lacinia tellus id mauris finibus lacus molestie",
          text4: "Curabitur a scelerisque ligula",
        },
        {
          title: "LATEST REPLIES",
          text1: "Nam a dolor volutpat massa auctor semper",
          text2: "Sed euismod nunc urna fermentum arcu dapibus fringilla",
          text3: "Cras lacinia tellus id mauris finibus lacus molestie",
          text4: "Curabitur a scelerisque ligula",
        },
      ],
    }
  },
}
</script>