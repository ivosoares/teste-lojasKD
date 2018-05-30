<template>
    <section class="view">
      <header class="results">
        <p><span>999</span>Resultados</p>
      </header>
      <div class="view-mode" id="teste">
        <p>Modo de exibição:</p>
        <a @click='changeMode("block")' class="btn active"><i class="fas fa-square"></i></a>
        <a @click='changeMode("list")' class="btn"><i class="fas fa-list-ul"></i></a>
        <a @click='changeMode("grid")' class="btn"><i class="fas fa-th"></i></a>
      </div>
    </section>
</template>
<script>
import eventbus from '../utils/events/eventbus'
export default {
  data () {
    return {
      viewMode: null
    }
  },
  methods: {
    changeMode (param) {
      var header = document.getElementById('teste')
      var btns = header.getElementsByClassName('btn')
      for (var i = 0; i < btns.length; i++) {
        btns[i].addEventListener("click", function() {
          var current = document.getElementsByClassName("active")
          current[0].className = current[0].className.replace(" active", "")
          this.className += " active"
        })
      }
      eventbus.$emit('clickbutton', param)
    }
  }
}
</script>
