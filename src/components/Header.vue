<template>
  <header >

    <nav>
      <div class="container">
        <div class="d-flex align-items-center justify-content-between">
          <a href="#"><img src="../assets/logo.png" alt="logo" class="_nav-logo"></a>

          <ul class="d-flex align-items-center ms-auto">
            <li v-for="(nav, i) in navbar" :key="i"><a :href="nav.link" class="_nav-link">{{nav.text}}</a></li>
          </ul>

          <a href="#" class="_btn-small _btn-black" style="margin: 0 20px">JOIN US</a>

          <i class="fa fa-search _nav-search" aria-hidden="true"></i>
 
        </div>
      </div>
    </nav>


    <section class="_hero">
      <div class="container">
        <h1>Tech Forum!</h1>
        <h4>Discuss all the latest technology news and trends</h4>
        <a href="#" class="_btn-medium _btn-blue">GET AVADA NOW! <span><i class="fa fa-chevron-right" aria-hidden="true"></i></span></a>
      </div>
    </section>

  </header>
</template>

<script>
export default {
  name: 'Header',
  data(){
    return{
      navbar: [
        {text: "Home", link: "/home"},
        {text: "Apple", link: "/apple"},
        {text: "Microsoft", link: "/microsoft"},
        {text: "Android", link: "/android"},
        {text: "Forums", link: "/forums"},
        {text: "Contact us", link: "/contact-us"},
      ],
    }
  },
}
</script>