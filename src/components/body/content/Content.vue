<template>
  <div class="content-font content-center">
      <h1>
          <p>Howdy!</p>
          <p>My name is
              <strong class="middle-blue-font">
                  Lauren
                </strong>
                and I'm a
                <strong class="middle-blue-font">
                    20 yo
                </strong>
            </p>
          <p>
              <vue-typer
                :text='["Software Engineering aspirant","Computer Engineering student","Agile and UX and design lover"," Software Development Intern","self-taught person"]'
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
          <p>from
              <strong class="middle-blue-font">
                  São Paulo, Brazil
                </strong>.
            </p>
</h1>
  </div>
</template>


<script>
import { VueTyper } from 'vue-typer'
export default {
    components: {
        'vue-typer': VueTyper
    }
}
</script>

<style scoped>

    .content-font {
        font-family: 'Coda', monospace;
        font-size: 0.9em;
        line-height: 0.4;
    }

    .content-center {
        margin-top: 5%;
        height: 70%;
        width: 100%;
        display: flex;
        position: fixed;
        align-items: center;
        text-align: center;
        justify-content: center;
    }

    .vue-typer {
        width: 10px;
        font-size: 1em;
        background-color: #1DA1EB;
    }
</style>