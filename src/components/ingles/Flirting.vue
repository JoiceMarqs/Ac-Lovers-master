<template>
  <section class="services " title="Paqueras" id="paqueras">
  <p><strong class="title "> Flirting</strong></p>
  <hr class="border ">
  <div class="q-pa-md">
    <div class="q-gutter-md">
      <q-carousel
        v-model="slide"
        transition-prev="jump-right"
        transition-next="jump-left"
        swipeable
        animated
        control-color="white"
        navigation
        padding
        arrows
        height="300px"
        class="shadow-1 rounded-borders" style="background:#aa96da;"
      >
        <q-carousel-slide name="style" class="column no-wrap flex-center">
          <div class="q-mt-md text-center">
            <q-img
                src="src\assets\apollo-head.png" style="width: 100px; height: 100px;" contain></q-img>
            {{ lorem }}
          </div>
        </q-carousel-slide>

        <q-carousel-slide name="layers" class="column no-wrap flex-center">
          <div class="q-mt-md text-center">
            <q-img
                src="src\assets\naomi-head.png" style="width: 100px; height: 100px;" contain></q-img>
            {{ lorem2 }}
          </div>
        </q-carousel-slide>
        <q-carousel-slide name="map" class="column no-wrap flex-center">
          <div class="q-mt-md text-center">
            <q-img
                src="src\assets\kae-head.png" style="width: 100px; height: 100px;" contain></q-img>
            {{ lorem3 }}
          </div>
        </q-carousel-slide>
      </q-carousel>
    </div>
  </div>
  <br>
  </section>
</template>

<script>
export default {
  data () {
    return {
      slide: 'style',
      lorem: 'Bad boy? T.I nerd? Fitting in labels or stereotypes is not something he likes, not when there are bugs to fix, games to win and one more note to decorate! Behind her dark circles and bad mood is a pure and understandable heart.',
      lorem2:'Owner of an energetic personality, she is never focused on just one thing. Some call her a mad scientist, others believe she should temper her ever-evident enthusiasm to show her best, but for who does she want to prove herself ?',
      lorem3:'Very popular with students for his kindness and talent, Kae is loved by all departments. His education and self-control means that he is always taking all eyes on himself. Despite this, he expresses all his mystery and feelings in his complex creations to understand, but still beautiful.'
    }
  }
}
</script>
