<template>
  <main>
    <!-- Section text -->
    <section class="_section-text _p-medium">
      <div class="container text-center">
        <h5>AVADA FORUM IS THE PLACE TO BE</h5>
        <p>In quis lectus sed leo elementum faucibus in dapibum dictum. <br>
          Nulla molestie tortor nec lectus venenatis, sed blandit dui finibus. <br>
          dolor at, bibendum purus. Donec vehicula nec tortor ac finibus.
        </p>
      </div>
    </section>

    <section class="container">
      <!-- Section Title -->
      <div class="_p-medium _section-title">
        <h5>PHASELLUS EGET METUS</h5>
        <h3>All the latest news</h3>
      </div>

      <!-- Section Preview Article Top -->
      <section class="row">
        <PreviewArticle
        v-for="(article, i) in previewArticleTop" :key="'previewArticleTop' + i"
        :img="article.img" :title="article.title" :subTitle="article.subTitle" :text="article.text">
        </PreviewArticle>
      </section>

      <!-- Section Jumbotron -->
      <section class="_section-jumbotron">
        <h5>FEATURED ARTICLE</h5>
        <h3>Cras malesauda et orci eget pharetra</h3>
        <p>In quis lectus sed leo elementum faucibus in dapibus dictum. Nullamolestie torto nec lectus venenatis, sed blandit dui, dolor at bibendum sadips ets ipsums dolores ficilis uns leo lectus.</p>
        <a href="#" class="_btn-medium _btn-black">READ MORE <span><i class="fa fa-chevron-right" aria-hidden="true"></i></span></a>
      </section>

      <!-- Section Preview Article Bottom -->
      <section class="row">
        <PreviewArticle
        v-for="(article, i) in previewArticleBottom" :key="'previewArticleBottom' + i"
        :img="article.img" :title="article.title" :subTitle="article.subTitle" :text="article.text">
        </PreviewArticle>
      </section>

      <!-- Section Tutorials & Guides -->
      <section class="container _section-tutorial-guide">
        <div class="row">

          <!-- Mini Jumbotron -->
          <div class="col-8 _section-jumbotron _section-mini-jumbotron">
            <h5>REVIEWED PRODUCT</h5>
            <h3>Mauris viverra atisan ipsum eget felis prims efficitur varius</h3>
            <p>In quis lectus sed leo elementum faucibus in dapibus dictum. Nullamolestie torto nec lectus venenatis, sed blandit dui, dolor at bibendum.</p>
            <a href="#" class="_btn-medium _btn-black">READ MORE <span><i class="fa fa-chevron-right" aria-hidden="true"></i></span></a>
          </div>

          <!-- Mini Preview Article -->
          <div class="col-4">
            <div class="_section-mini-preview-article">
              <h3>Tutorials & Guides</h3>
              
              <div class="_mini-preview-article d-flex flex-column justify-content-end">
                <div v-for="(miniPreview, i) in miniPreviewArticle" :key="'mini-preview' + i" class="d-flex">
                  <img :src="miniPreview.img" alt="">
                  <div class="_text-mini-preview">
                    <h5> {{miniPreview.title}} </h5>
                    <h4> {{miniPreview.subTitle}} </h4>
                  </div>
                </div>
              </div>

            </div>
          </div>
        </div>
      </section>
    </section>

    <!-- Banner Black -->
    <section class="_section-banner-black">
      <div class="container">
        <a href="#">
          <h4>READ OUR BLOG <i class="fa fa-long-arrow-right" aria-hidden="true"></i> </h4>
        </a>
      </div>
    </section>

    <!-- Section Forum -->
    <section class="_section-forum">
      <div class="container">
        <!-- Section Title -->
        <div class="_p-medium _section-title">
          <h5>PHASELLUS EGET METUS</h5>
          <h3>Forum Section</h3>
        </div>

        <!-- Section Card Forum -->
        <div class="row g-5 _section-forum-card">
          <ForumCard
          v-for="(card, i) in forumCard" :key="'forum-card'+ i"
          :title="card.title" :icon="card.icon"
          ></ForumCard>
        </div>

      </div>
    </section>

    <!-- Banner Black -->
    <section class="_section-banner-black">
      <div class="container">
        <a href="#">
          <h4>GO TO OUR FORUM <i class="fa fa-long-arrow-right" aria-hidden="true"></i> </h4>
        </a>
      </div>
    </section>

    <!-- Section Community -->
    <section class="_section-community _p-large">
      <div class="container text-center m-auto">
        <h3>HEY! Join to our<br>Community</h3>
        <p>Nulla molestie tortor nec lectus venenatis, sed blandit dui finibus. Curabitur feugiat<br>vulputate purus ipsums dolores ficilis etra.</p>
        <a href="#" class="_btn-medium _btn-blue">SIGN UP<span><i class="fa fa-chevron-right" aria-hidden="true"></i></span></a>
      </div>
    </section>

  </main>
</template>

<script>
import PreviewArticle from './PreviewArticle.vue'
import ForumCard from './ForumCard.vue'

export default {
  name: 'Main',
  components: {PreviewArticle, ForumCard},
  data(){
    return{
      previewArticleTop: [
        { 
          img: require("../assets/post_feat_img_25-320x202.jpg"),
          title: "Morbi vitae dui euismod vulputate sollicitudin",
          subTitle: "October 11th, 2015 | 2 Comments",
          text: "Donec finibus sit amet orci eget ultricies. Prasent posuere ante ut erat fringilla, vestibulum placerat metus mattis. Aenean dictum vitae nisl"
          },
        { 
          img: require("../assets/post_feat_img_24-320x202.jpg"),
          title: "Vivamus pellenteque, felis qui varius",
          subTitle: "October 11th, 2015 | Comments Off",
          text: "Donec finibus sit amet orci eget ultricies. Prasent posuere ante ut erat fringilla, vestibulum placerat metus mattis. Aenean dictum vitae nisl"
          },
        { 
          img: require("../assets/post_feat_img_23-320x202.jpg"),
          title: "Donec ornare pretium eget scelisque justo",
          subTitle: "October 11th, 2015 | Comments Off",
          text: "Donec finibus sit amet orci eget ultricies. Prasent posuere ante ut erat fringilla, vestibulum placerat metus mattis. Aenean dictum vitae nisl"
          },
      ],
      previewArticleBottom: [
        { 
          img: require("../assets/post_feat_img_22-320x202.jpg"),
          title: "Fusce sollicitudin nunc sed placerat varius",
          subTitle: "October 11th, 2015 | Comments Off",
          text: "Donec finibus sit amet orci eget ultricies. Prasent posuere ante ut erat fringilla, vestibulum placerat metus mattis. Aenean dictum vitae nisl"
          },
        { 
          img: require("../assets/post_feat_img_21-320x202.jpg"),
          title: "Donec facilis sodales leo sit amet laoreet",
          subTitle: "October 11th, 2015 | Comments Off",
          text: "Donec finibus sit amet orci eget ultricies. Prasent posuere ante ut erat fringilla, vestibulum placerat metus mattis. Aenean dictum vitae nisl"
          },
        { 
          img: require("../assets/post_feat_img_20-320x202.jpg"),
          title: "Proin eu purus sed aru aliquet curabir vens",
          subTitle: "October 11th, 2015 | Comments Off",
          text: "Donec finibus sit amet orci eget ultricies. Prasent posuere ante ut erat fringilla, vestibulum placerat metus mattis. Aenean dictum vitae nisl"
          },
      ],
      miniPreviewArticle: [
        {
          img: require("../assets/post_feat_img_23-177x142.jpg"),
          title: "Donec ornare pretium eget scelisque justo",
          subTitle: "October 11th, 2015 | Comments Off",
        },
        {
          img: require("../assets/post_feat_img_22-147x118.jpg"),
          title: "Fusce sollicitudin nunc sed placerat varius",
          subTitle: "October 11th, 2015 | Comments Off",
        },
        {
          img: require("../assets/post_feat_img_20-177x142.jpg"),
          title: "Proin eu purus sed aru aliquet curabir vens",
          subTitle: "October 11th, 2015 | Comments Off",
        },
      ],
      featuredArticleLarge : {
          img: require("../assets/featured_article_1_bg.jpg"),
          title: "FEATURED ARTICLE",
          subTitle: "Cras malesauda et orci eget pharetra",
          text: "In quis lectus sed leo elementum faucibus in dapibus dictum. Nullamolestie torto nec lectus venenatis, sed blandit dui, dolor at bibendum sadips ets ipsums dolores ficilis uns leo lectus.",
          btn: "READ MORE",
      },
      forumCard: [
        {
          title: "News & Community",
          icon: "fa fa-file-text",
        },
        {
          title: "Apple Forum",
          icon: "fa fa-apple",
        },
        {
          title: "Microsoft Forum",
          icon: "fa fa-windows",
        },
        {
          title: "Android Forum",
          icon: "fa fa-android",
        },
        {
          title: "General Discussion",
          icon: "fa fa-coffee",
        },
        {
          title: "App & Software",
          icon: "fa fa-cubes",
        },
        {
          title: "Gadgets & Stuff",
          icon: "fa fa-laptop",
        },
        {
          title: "Tutorials & Guides",
          icon: "fa fa-wrench",
        },
      ],
    }
  },
}
</script>