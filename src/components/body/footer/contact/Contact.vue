<template>
  <div class="l-contact">
      <div></div>
      <div class="social-media">
                <a href="mailto:lauren.ferremch@gmail.com" title="Mail me!" target="_blank"><strong><i class="fa fa-envelope"></i></strong></a>
                <a href="https://www.linkedin.com/in/lauren-ferreira-9836914b/" title="My professional experiences and courses" target="_blank"><strong><i class="fa fa-linkedin"></i></strong></a>
                <a href="https://github.com/laurenmariaferreira" title="More of my coding projects" target="_blank"><strong><i class="fa fa-github"></i></strong></a>
                <a href="http://www.twitter.com/larienmf" title="Come see my tweets!" target="_blank"><strong><i class="fa fa-twitter"></i></strong></a>
        </div>
        <div></div>
  </div>

  
</template>


<script>
export default {
  
}
</script>


<style scoped>
    .social-media {
    display:flex;
    flex-wrap:wrap;
    text-align:center;
    margin:auto;
    justify-content: center;
    }

    .fa {
    margin: 5px;
    padding: 5px;
    border-radius: 10%;
    background: #1B2836;
    color: #808F9A;
    transition: border 0.1s, color 0.3s, background 0.3s;
    }

    .fa-envelope:hover {
    background: #A3333D;
    color: white;
    }

    .fa-github:hover {
    background: #111111;
    color: white;
    }

    .fa-linkedin:hover {
    background: #0077B5;
    color: white;
    }

    .fa-twitter:hover {
    background: #55ACEE;
    color: white;
    }
</style>