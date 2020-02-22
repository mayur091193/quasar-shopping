<template>
  <q-page>
    <div class="row q-col-gutter-sm">
      <div class="col-lg-12 col-md-12 col-sm-12 col-xs-12">
        <q-carousel
          arrows
          animated
          v-model="slide"
          height="250px"
        >
          <q-carousel-slide name="first" img-src="https://cdn.quasar.dev/img/mountains.jpg">
            <div class="absolute-bottom custom-caption">
              <div class="text-subtitle1">First stop</div>
              <div class="text-caption">Mountains</div>
            </div>
          </q-carousel-slide>
          <q-carousel-slide name="second" img-src="https://cdn.quasar.dev/img/parallax1.jpg">
            <div class="absolute-bottom custom-caption">
              <div class="text-subtitle1">Second stop</div>
              <div class="text-caption">Famous City</div>
            </div>
          </q-carousel-slide>
          <q-carousel-slide name="third" img-src="https://cdn.quasar.dev/img/parallax2.jpg">
            <div class="absolute-bottom custom-caption">
              <div class="text-subtitle1">Third stop</div>
              <div class="text-caption">Famous Bridge</div>
            </div>
          </q-carousel-slide>
        </q-carousel>
      </div>
    </div>

  </q-page>
</template>


<script>
    export default {
        data() {
            return {
                slide: 'first'
            }
        },
        methods: {}
    }
</script>

<style scoped>
  .custom-caption {
    text-align: center;
    padding: 8px;
    color: white;
    background-color: rgba(0, 0, 0, .3);
  }

</style>
