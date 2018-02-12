<template>
  <div class="l-contact">
      <div></div>
      <div v-if="!languageSelector" class="social-media">
                <a
                class="fa fa-envelope"
                title="Mail me!"
                href="mailto:lauren.ferremch@gmail.com"
                target="_blank"
                ><strong><i></i></strong></a>
                <a
                class="fa fa-linkedin"
                title="My professional experiences and courses"
                href="https://www.linkedin.com/in/lauren-ferreira-9836914b/"
                target="_blank"
                ><strong><i></i></strong></a>
                <a
                class="fa fa-github"
                title="More of my coding projects"
                href="https://github.com/laurenmariaferreira"
                target="_blank"
                ><strong><i></i></strong></a>
                <a
                class="fa fa-twitter"
                title="Come see my tweets!"
                href="http://www.twitter.com/larienmf"
                target="_blank"
                ><strong><i></i></strong></a>
        </div>
        <div v-else class="social-media">
                <a
                class="fa fa-envelope"
                title="Me envie um e-mail!"
                href="mailto:lauren.ferremch@gmail.com"
                target="_blank"
                ><strong><i></i></strong></a>
                <a
                class="fa fa-linkedin"
                title="Minhas experiências profissionais e certificações"
                href="https://www.linkedin.com/in/lauren-ferreira-9836914b/"
                target="_blank"
                ><strong><i></i></strong></a>
                <a
                class="fa fa-github"
                title="Mais projetos desenvolvidos por mim"
                href="https://github.com/laurenmariaferreira"
                target="_blank"
                ><strong><i></i></strong></a>
                <a
                class="fa fa-twitter"
                title="Acompanhe meus tweets!"
                href="http://www.twitter.com/larienmf"
                target="_blank"
                ><strong><i></i></strong></a>
        </div>
        <div v-if="!languageSelector" class="version">
            <p title="2.2 Version number">v2.2</p>
        </div>
        <div v-else class="version">
            <p title="2.2 Inserção do número de versão">v2.2</p>
        </div>
  </div>
</template>

<script>
import EventBus from '../../../../eventbus.js';
export default {
  data() {
      return {
         languageSelector: false,
      }
    },
    created() {
    EventBus.$on('change_language', () => {
        this.changeLanguage()
    })
    },
        methods: {
    changeLanguage(){
        this.languageSelector = !this.languageSelector;
    }
}
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

    a {
    margin: 5px;
    padding: 8px;
    border-radius: 10%;
    background: #1B2836;
    color: #808F9A;
    transition: border 0.1s, color 0.3s, background 0.3s;
    text-decoration: none;
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

    .version {
        position: absolute;
        font-size: 10px;
        color: #808F9A;
        bottom: 0;
        right: 0;
    }

    @media (max-width: 700px) 
{
  .fa {
    padding: 15px;
    border-radius: 10%;
    background: #1B2836;
    color: #808F9A;
    transition: border 0.1s, color 0.3s, background 0.3s;
    text-decoration: none;
  }
}
</style>