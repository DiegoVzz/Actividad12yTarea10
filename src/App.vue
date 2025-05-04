<template>
  <div class="app">
    <h1 class="title">Datos curiosos Chuck Norris</h1>
    
    <!-- Sección original -->
    <div class="facts-container">
      <div 
        v-for="(fact, index) in chuckFacts" 
        :key="index" 
        class="fact-card"
        :class="{'odd-card': index % 2, 'even-card': !(index % 2)}"
      >
        <p class="fact-text">{{ fact.value }}</p>
      </div>
    </div>

    <!-- Nueva sección con Bootstrap -->
    <div class="container mt-5">
      <h2 class="text-center mb-4">Nuevas Tarjetas con Imagen</h2>
      <div class="row">
        <div 
          v-for="(item, index) in chuck" 
          :key="index" 
          class="col-12 col-md-6 col-lg-4 mb-4"
        >
          <chuck-card 
            :icon_url="item.icon_url" 
            :value="item.value"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ChuckCard from './components/ChuckCard.vue'

export default {
  name: 'App',
  components: {
    ChuckCard
  },
  data() {
    return {
      // Datos originales
      chuckFacts: [
        { "value": "Chuck Norris puede saltar en paracaídas al espacio exterior." },
        { "value": "El principal producto de Chuck Norris es el dolor." },
        { "value": "Chuck Norris no lee libros. Los mira fijamente hasta que obtiene la información que quiere." },
        { "value": "El tiempo no espera a nadie. A menos que ese hombre sea Chuck Norris." },
        { "value": "Si escribes Chuck Norris en Scrabble, ganas. Para siempre." }
      ],
      
      // Nuevos datos
      chuck: [
        {
          "icon_url": "https://assets.chucknorris.host/img/avatar/chuck-norris.png",
          "value": "Chuck Norris puede saltar en paracaídas al espacio exterior."
        },
        {
          "icon_url": "https://assets.chucknorris.host/img/avatar/chuck-norris.png",
          "value": "El principal producto de Chuck Norris es el dolor."
        },
        {
          "icon_url": "https://assets.chucknorris.host/img/avatar/chuck-norris.png",
          "value": "Chuck Norris no lee libros. Los mira fijamente hasta que encuentra la información que busca."
        },
        {
          "icon_url": "https://assets.chucknorris.host/img/avatar/chuck-norris.png",
          "value": "El tiempo no espera a nadie. A menos que ese hombre sea Chuck Norris."
        },
        {
          "icon_url": "https://assets.chucknorris.host/img/avatar/chuck-norris.png",
          "value": "Si deletreas Chuck Norris en Scrabble, ganas. Para siempre."
        }
      ]
    }
  }
}
</script>