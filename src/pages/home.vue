<template>
  <q-page class="q-mt-sm">
    <div class="row q-col-gutter-sm">
      <div class="col-lg-10 col-md-10 col-sm-12 col-xs-12">
        <q-carousel
          class="q-ml-sm"
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
      <div class="col-md-2">
        <q-card class="bg-white q-mr-sm q-pt-sm">
          <img src="https://www.graphicsprings.com/filestorage/stencils/d3dd5cb632e0826d9e6136af3241b28e.png" style="margin:auto;width:66%;">
          <q-card-section class="q-pt-xs">
            <div class="text-caption text-center text-grey-7">Your Delivery Pincode</div>
            <div class="text-caption text-center q-mt-sm text-grey-9">Enter your pincode to check availability and
              faster options
            </div>
            <div class="q-mt-sm">
              <q-input dense outlined placeholder="Enter pincode"></q-input>
            </div>
            <div class="q-mt-xs">
              <div style="display:block; height:22px;">
                <q-btn size="sm" label="Save" class="q-mt-xs text-capitalize bg-primary text-white float-right"/>
              </div>
            </div>
          </q-card-section>
        </q-card>
      </div>
    </div>
    <div class="text-grey-9 text-weight-bold">
      <div class="row items-center q-mx-sm">
        <div class="col-12 q-mt-sm">
          <div class="q-pl-md bg-white q-pt-sm ">
            <span class="text-grey-9 text-h6 text-weight-bold">Latest Launches</span> <a
            class="text-primary q-ml-sm cursor-pointer">[see all]</a>
          </div>
          <q-carousel
            v-model="latest_slide"
            transition-prev="slide-right"
            transition-next="slide-left"
            swipeable
            animated
            control-color="primary"
            navigation
            padding
            arrows
            height="260px"
            class="rounded-borders"
          >
            <q-carousel-slide v-for="val in [1,2,3]" :name="val" class="column no-wrap">
              <div class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap">
                <div @click="$router.push('/details')" class="col-2 hover_border_grey text-center full-height">
                  <q-img style="" class="rounded-borders"
                         src="https://www.graphicsprings.com/filestorage/stencils/d3dd5cb632e0826d9e6136af3241b28e.png">
                  </q-img>
                  <div>Redmi 8</div>
                  <div class="text-caption text-weight-bold text-green">5000h mAh Battery</div>
                  <div><span>₹8,499</span><span class="q-ml-sm text-grey-6" style="text-decoration: line-through">₹10,999</span>
                  </div>
                </div>
                <div @click="$router.push('/details')" class="col-2 hover_border_grey text-center full-height">
                  <q-img style="" class="rounded-borders"
                         src="https://www.graphicsprings.com/filestorage/stencils/d3dd5cb632e0826d9e6136af3241b28e.png">
                  </q-img>
                  <div>Redmi 8</div>
                  <div class="text-caption text-weight-bold text-green">5000h mAh Battery</div>
                  <div><span>₹8,499</span><span class="q-ml-sm text-grey-6" style="text-decoration: line-through">₹10,999</span>
                  </div>
                </div>
                <div @click="$router.push('/details')" class="col-2 hover_border_grey text-center full-height">
                  <q-img style="" class="rounded-borders"
                         src="https://www.graphicsprings.com/filestorage/stencils/d3dd5cb632e0826d9e6136af3241b28e.png">
                  </q-img>
                  <div>Redmi 8</div>
                  <div class="text-caption text-weight-bold text-green">5000h mAh Battery</div>
                  <div><span>₹8,499</span><span class="q-ml-sm text-grey-6" style="text-decoration: line-through">₹10,999</span>
                  </div>
                </div>
                <div @click="$router.push('/details')" class="col-2 hover_border_grey text-center full-height">
                  <q-img style="" class="rounded-borders"
                         src="https://www.graphicsprings.com/filestorage/stencils/d3dd5cb632e0826d9e6136af3241b28e.png">
                  </q-img>
                  <div>Redmi 8</div>
                  <div class="text-caption text-weight-bold text-green">5000h mAh Battery</div>
                  <div><span>₹8,499</span><span class="q-ml-sm text-grey-6" style="text-decoration: line-through">₹10,999</span>
                  </div>
                </div>
                <div @click="$router.push('/details')" class="col-2 hover_border_grey text-center full-height">
                  <q-img style="" class="rounded-borders"
                         src="https://www.graphicsprings.com/filestorage/stencils/d3dd5cb632e0826d9e6136af3241b28e.png">
                  </q-img>
                  <div>Redmi 8</div>
                  <div class="text-caption text-weight-bold text-green">5000h mAh Battery</div>
                  <div><span>₹8,499</span><span class="q-ml-sm text-grey-6" style="text-decoration: line-through">₹10,999</span>
                  </div>
                </div>
                <div class="col-2 hover_border_grey text-center full-height">
                  <q-img style="" class="rounded-borders"
                         src="https://www.graphicsprings.com/filestorage/stencils/d3dd5cb632e0826d9e6136af3241b28e.png">
                  </q-img>
                  <div>Redmi 8</div>
                  <div class="text-caption text-weight-bold text-green">5000h mAh Battery</div>
                  <div><span>₹8,499</span><span class="q-ml-sm text-grey-6" style="text-decoration: line-through">₹10,999</span>
                  </div>
                </div>
              </div>
            </q-carousel-slide>
          </q-carousel>
        </div>
      </div>
      <div class="row items-center q-mx-sm">
        <div class="col-12 q-mt-sm">
          <div class="q-pl-md bg-white q-pt-sm">
            <span class="text-grey-9 text-h6 text-weight-bold">Trending in</span> <a
            class="text-primary q-ml-sm cursor-pointer">[see more]</a>
          </div>
          <q-carousel
            v-model="trending_slide"
            transition-prev="slide-right"
            transition-next="slide-left"
            swipeable
            animated
            control-color="primary"
            navigation
            padding
            arrows
            height="260px"
            class="rounded-borders"
          >
            <q-carousel-slide v-for="val in [1,2,3]" :name="val" class="column no-wrap">
              <div class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap">
                <q-img @click="$router.push('/category')" style="border:1px solid lightgrey;" class="rounded-borders col-3 cursor-pointer full-height"
                       src="https://www.graphicsprings.com/filestorage/stencils/1cdf3eae16b6d0da3f16ff12f7650a24.png">
                  <div class="absolute-bottom custom-caption" style="background-color:rgba(0, 0, 0, .5);">
                    <div class="text-caption text-weight-bolder">Electronics</div>
                  </div>
                </q-img>
                <q-img @click="$router.push('/category')" style="border:1px solid lightgrey;" class="rounded-borders col-3 cursor-pointer full-height"
                       src="https://www.graphicsprings.com/filestorage/stencils/d3dd5cb632e0826d9e6136af3241b28e.png">
                  <div class="absolute-bottom custom-caption" style="background-color:rgba(0, 0, 0, .5);">
                    <div class="text-caption text-weight-bolder">TVs and Appliances</div>
                  </div>
                </q-img>
                <q-img @click="$router.push('/category')" style="border:1px solid lightgrey;" class="rounded-borders col-3 cursor-pointer full-height"
                       src="https://www.graphicsprings.com/filestorage/stencils/1cdf3eae16b6d0da3f16ff12f7650a24.png">
                  <div class="absolute-bottom custom-caption" style="background-color:rgba(0, 0, 0, .5);">
                    <div class="text-caption text-weight-bolder">Men</div>
                  </div>
                </q-img>
                <q-img @click="$router.push('/category')" style="border:1px solid lightgrey;" class="rounded-borders col-3 cursor-pointer full-height"
                       src="https://www.graphicsprings.com/filestorage/stencils/d3dd5cb632e0826d9e6136af3241b28e.png">
                  <div class="absolute-bottom custom-caption" style="background-color:rgba(0, 0, 0, .5);">
                    <div class="text-caption text-weight-bolder">Women</div>
                  </div>
                </q-img>
              </div>
            </q-carousel-slide>
          </q-carousel>
        </div>
      </div>
      <div class="row q-mt-sm q-mx-sm bg-white text-center">
        <div class="col-2" style="border-right: 1px solid lightgrey"></div>
        <div class="col-2" style="border-right: 1px solid lightgrey">
          <q-img src="https://www.graphicsprings.com/filestorage/stencils/3055581cff0526602142cbb0bfba9fca.png"></q-img>
          <div class="text-subtitle1 q-mb-sm text-grey-8">100% Secure Payments</div>
        </div>
        <div class="col-2" style="border-right: 1px solid lightgrey">
          <q-img src="https://www.graphicsprings.com/filestorage/stencils/3055581cff0526602142cbb0bfba9fca.png"></q-img>
          <div class="text-subtitle1 q-mb-sm text-grey-8">Trustpay</div>
        </div>
        <div class="col-2" style="border-right: 1px solid lightgrey">
          <q-img src="https://www.graphicsprings.com/filestorage/stencils/3055581cff0526602142cbb0bfba9fca.png"></q-img>
          <div class="text-subtitle1 q-mb-sm text-grey-8">Help Center</div>
        </div>
        <div class="col-2" style="border-right: 1px solid lightgrey">
          <q-img src="https://www.graphicsprings.com/filestorage/stencils/3055581cff0526602142cbb0bfba9fca.png"></q-img>
          <div class="text-subtitle1 q-mb-sm text-grey-8">Shop On The Go</div>
        </div>
      </div>

    </div>
  </q-page>
</template>


<script>
  import Vue from 'vue';

  export default {
    data() {
      return {
        slide: 'first',
        trending_slide: 1,
        latest_slide: 1
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
