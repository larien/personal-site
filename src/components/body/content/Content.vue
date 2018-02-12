<template>
  <div class="content-font content-center">
      <h1>
          <div v-if="!languageSelector">
          <p>Howdy!</p>
          <p>My name is
              <strong class="middle-blue-font">
                  Lauren
                </strong>
                and I'm a
                <strong class="middle-blue-font">
                    {{ calcAge }} yo
                </strong>
            </p>
          <p>
              <vue-typer
                :text='[" Software Engineering aspirant ",
                " Computer Engineering student ",
                " Agile, UX and design lover ",
                " Software Development Intern ",
                " self-taught person ",
                " Korra fangirl "]'
                :repeat='Infinity'
                :shuffle='true'
                initial-action='typing'
                :pre-type-delay='50'
                :type-delay='50'
                :pre-erase-delay='2000'
                :erase-delay='100'
                erase-style='backspace'
                :erase-on-complete='true'
                caret-animation='smooth'
                ></vue-typer>
          </p>
          <p>from
              <strong class="middle-blue-font">
                  São Paulo, Brazil
                </strong>.
            </p>
        </div>
        <div v-else>
          <p>Olá!</p>
          <p>Meu nome é
              <strong class="middle-blue-font">
                  Lauren
                </strong>
                .
            </p>
            <p>Tenho
                <strong class="middle-blue-font">
                  {{ calcAge }} anos
                </strong>
                e sou uma
            </p>
          <p>
              <vue-typer
                :text='[" futura Engenheira de Software ",
                " estudante de Engenharia de Computação ",
                " amante de Agile, UX e design ",
                " mulher autodidata ",
                " fangirl da Korra "]'
                :repeat='Infinity'
                :shuffle='true'
                initial-action='typing'
                :pre-type-delay='70'
                :type-delay='70'
                :pre-erase-delay='3000'
                :erase-delay='100'
                erase-style='backspace'
                :erase-on-complete='true'
                caret-animation='smooth'
                ></vue-typer>
          </p>
          <p>de
              <strong class="middle-blue-font">
                  São Paulo, Brasil
                </strong>.
            </p>
            </div>
</h1>
  </div>
</template>


<script>
import { VueTyper } from 'vue-typer';
import EventBus from '../../../eventbus.js';

export default {
    components: {
        'vue-typer': VueTyper
    },
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
computed: {
    calcAge: function () {
    var y = 1997, m = 8, d = 5;

    var date = new Date,
        aa = date.getFullYear(),
        ma = date.getMonth() + 1,
        da = date.getDate(),

        y = +y,
        m = +m,
        d = +d,
        idade = aa - y;

    if (ma < m || ma == m && da < d) {
            idade--;
    }
    
    return idade < 0 ? 0 : idade;
    }
},
methods: {
    changeLanguage(){
        this.languageSelector = !this.languageSelector;
    }
}
   
}
</script>

<style scoped>

    .content-font {
        font-family: 'Coda', monospace;
        text-align: center;
        line-height: 130%;
        font-size: 4vh;
    }

    .content-center {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .vue-typer {
        width: 10px;
        background-color: #1DA1EB;
    }
</style>