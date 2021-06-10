

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
      <h3 class="nombreTrastorno">Ansiedad</h3>
      <div class="trastorno">
        <h1 class="cifra">15%</h1>
        <h3 class="datoTrastorno">3 veces más de lo habitual</h3>
      </div>
      <h3 class="nombreTrastorno">Depresión</h3>
      <div class="trastorno">
        <h1 class="cifra">16%</h1>
        <h3 class="datoTrastorno">4 veces más de lo habitual</h3>
      </div>
      <h3 class="nombreTrastorno">Estrés Postraumático</h3>
      <div class="trastorno">
        <h1 class="cifra">22%</h1>
        <h3 class="datoTrastorno">5 veces más de lo habitual</h3>
      </div>
      <h3 class="nombreTrastorno">Insomnio</h3>
      <div class="trastorno">
        <h1 class="cifra">24%</h1>
      </div>
    </div>

    <div class="container5" id="trigger5">
      <p class="oms">
        OMS, 10/2020: Informa de que la crisis del COVID ha paralizado o
        perturbado los servicios de salud mental críticos en el 93% de países
        del mundo.
      </p>
    </div>

    <div class="container6">
      <h1 class="tit_españa">¿Y en España?</h1>

      <h3 class="nombreTrastorno">Ansiedad</h3>
      <div class="trastorno">
        <h1 class="cifra">6,7%</h1>
      </div>
      <h3 class="nombreTrastorno">Depresión</h3>
      <div class="trastorno">
        <h1 class="cifra">6,7%</h1>
        <h3 class="datoTrastorno">
          En 2050 será el principal problema de salud.
        </h3>
      </div>
      <h3 class="nombreTrastorno">Problemas de sueño</h3>
      <div class="trastorno">
        <h1 class="cifra">41,9%</h1>
        <h3 class="datoTrastorno">5 veces más de lo habitual</h3>
      </div>
      <h3 class="nombreTrastorno">Suicidios</h3>
      <div class="trastorno">
        <h1 class="cifra">24%</h1>
        <h3 class="datoTrastorno">
          Aumentó un 50% más de consultas sobre suicidios a los teléfonos de la
          esperanza
        </h3>
      </div>
      <h3 class="nombreTrastorno">Personas con trastornos mentales graves</h3>
      <div class="trastorno">
        <h1 class="cifra larga">1.000.000</h1>
      </div>

      
      <div class="hospiDelMar">
        <img class="hospiMarImg" src="./img/3hospitalMar.jpg" alt="" />
        <p class="delMarText">
          Las personas que han sufrido trastornos mentales previos a la
          pandemia, los sanitarios que han estado más expuestos a la covid, los
          profesionales que se infectaron o tuvieron que hacer cuarentena y las
          auxiliares de enfermería son los colectivos de mayor riesgo y deben
          considerarse “grupos que necesitan seguimiento y apoyo a su salud
          mental”.
        </p>
        <p class="cita">-Hospital del Mar de Barcelona</p>
      </div>
    </div>

    <div class="container7">
      <div class="slides">
        <h1>Los más vulnerables</h1>
        <img class="flechaDrcha" src="./img/7flechadrcha.png" alt="" />
        <h2>Los sanitarios</h2>
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
      .setPin(".mundoimg")
      .addTo(controller);

    var scene5 = new this.$scrollmagic.Scene({
      triggerElement: "#trigger5",
      triggerHook: 0.3, // show, when scrolled 10% into view
      duration: "80%", // hide 10% before exiting view (80% + 10% from bottom)
      offset: 90, // move trigger to center of element
    })
      .setClassToggle(".oms", "visible") // add class to reveal
      .addIndicators() // add indicators (requires plugin)
      .addTo(controller);

    var scene7 = new this.$scrollmagic.Scene({
      triggerElement: ".hospiMarImg",
      duration: 500,
      offset: 250,
    })
      .setPin(".hospiMarImg")
      .addTo(controller);

    var scene8 = new this.$scrollmagic.Scene({
      triggerElement: ".delMarText",
      duration: 500,
      offset: 170,
    })
      .setPin(".delMarText")
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
