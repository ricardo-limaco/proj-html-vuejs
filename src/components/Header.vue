<template>
  <div>
    
  </div>
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