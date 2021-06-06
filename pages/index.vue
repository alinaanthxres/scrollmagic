<template>
  <div>
    <div class="intro_1">
      <h1 class="intro_h1" @click="hola">
        <u>Más allá del COVID:</u><br />
        Por qué nos estamos enfrentando a una pandemia de salud mental
      </h1>

      <p class="intro_p p1" id="animate1">
        La pandemia del COVID_19 ha tenido un impacto muy grande en nuestras
        vidas.
      </p>
      <p class="intro_p p2" id="animate1">
        Muchos de nosotros nos hemos enfrentado a complicaciones estresantes y
        sobrecogedoras, y aunque la campaña de vacunación nos trae algo de
        calma, debemos cuidarnos para las consecuencias en la salud mental que
        ha dejado el virus.
      </p>
      <p class="intro_p p3" id="animate1">Las causas son varias:</p>
    </div>

    <div class="container2">
      <div class="causas">
        <ul class="listaCausas">
          <li class="causa">Confinamiento y asilamiento total</li>
          <li class="causa">Problemas financieros</li>
          <li class="causa">Distanciamiento físico y social</li>
          <li class="causa">Temor al contagio</li>
          <li class="causa">Preocupación por familiares y amigos</li>
          <li class="causa">Incertidumbre</li>
          <li class="causa">Alto número de fallecimientos</li>
        </ul>
      </div>
    </div>

      <div class="container3">
        <h1 class="mundo">
          ¿Cómo lo <br />
          hemos vivido <br />
          en todo el mundo?
        </h1>
        <img class="mundoimg" src="./img/2tierra.gif" alt="" />
        <div class="subtitulo">
          <h3 class="trastorno">
            1.000.000.000 personas padecen un trastorno mental
          </h3>
          <h3 class="datos">Los últimos datos:</h3>
        </div>
      </div>
      
      <div class="container4">
        <div class="trastorno">
          <h3 class="nombreTrastorno">Ansiedad</h3>
          <h1 class="cifra">15%</h1>
          <h3 class="datoTrastorno">3 veces más de lo habitual</h3>
        </div>
        <div class="trastorno">
          <h3 class="nombreTrastorno">Depresión</h3>
          <h1 class="cifra">16%</h1>
          <h3 class="datoTrastorno">4 veces más de lo habitual</h3>
        </div>
        <div class="trastorno">
          <h3 class="nombreTrastorno">Estrés Postraumático</h3>
          <h1 class="cifra">22%</h1>
          <h3 class="datoTrastorno">5 veces más de lo habitual</h3>
        </div>
        <div class="trastorno">
          <h3 class="nombreTrastorno">Insomnio</h3>
          <h1 class="cifra">24%</h1>
        </div>
      </div>


    <div class="hola"></div>
  </div>
</template>

<script>
export default {
  mounted() {
    const controller = new this.$scrollmagic.Controller();

    var scene = new this.$scrollmagic.Scene({
      triggerElement: ".p1",
    })
      // trigger a TweenMax.to tween
      .setTween("#animate1", 0.5, { rotate: 4 })
      .addIndicators()
      .addTo(controller);

    var scene2 = new this.$scrollmagic.Scene({
      triggerElement: ".mundoimg",
      duration: 350,
    })
      // trigger a TweenMax.to tween
      .setPin(".mundoimg")
      // add indicators (requires plugin)
      //.addIndicators({name: "1 (duration: 300)"})
      //.setTween("#animate2", 0.5, {backgroundColor: "white"})
      .addTo(controller);


    var backgroundSec3 = new this.$scrollmagic.Scene({triggerElement: ".mundoimg", duration: 500})
      .setTween("#sec3", 3, {backgroundColor: "rgba(0, 19, 187, 1)"})
      .addIndicators() // add indicators (requires plugin)
      .addTo(controller);
  },
  methods: {
    hola() {
      alert("hola");
    },
  },
};
</script>

<style lang="scss">
</style>
