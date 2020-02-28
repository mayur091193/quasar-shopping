<template>
  <div class="row bg-white q-mt-sm">
    <div class="col-5">
      <div class="q-pa-md">

        <ProductZoomer
          :base-images="images"
          :base-zoomer-options="zoomerOptions"
        />
        <q-carousel
          swipeable
          animated
          v-model="slide"
          thumbnails
          infinite
        >
          <q-carousel-slide :name="1" img-src="https://cdn.quasar.dev/img/mountains.jpg"/>
          <q-carousel-slide :name="2" img-src="https://cdn.quasar.dev/img/parallax1.jpg"/>
          <q-carousel-slide :name="3" img-src="https://cdn.quasar.dev/img/parallax2.jpg"/>
          <q-carousel-slide :name="4" img-src="https://cdn.quasar.dev/img/quasar.jpg"/>
        </q-carousel>

        <div>
          <q-btn class="q-mt-md" color="orange-9" icon="shopping_cart" label="Add to cart"/>
          <q-btn class="q-mt-md q-ml-md" color="orange-8" icon="shopping_cart" label="Buy now"/>
        </div>
      </div>
    </div>
    <div class="col-7">
      <div class="text-subtitle1 text-grey-10 q-mt-sm q-pt-xs">Benling C200-BLK Smartwatch (Black Strap Free Size)</div>
      <div>
        <q-chip size="10px" class="text-weight-bold q-px-xs" square color="green-7" text-color="white"
                icon-right="star">
          4.4
        </q-chip>
        <span class="text-caption text-weight-bold text-grey-6">6 Ratings & 2 Reviews</span>
      </div>
      <div>
        <div class="text-caption text-green-8 text-weight-bolder q-mt-sm">Special Price</div>
        <span class="text-h6">₹3,149</span><span class="q-ml-sm text-grey-6" style="text-decoration: line-through">₹3,699</span>
        <span class="q-ml-md text-caption text-green-8 text-weight-bolder q-mt-md">20% off</span>
      </div>
      <div class="q-mt-sm text-weight-bold">
        Offers
        <ul class="q-pl-sm text-caption" style="list-style-type: none">
          <li class="q-mt-xs"><span class="text-weight-bold">Bank Offer</span> 5% Unlimited Cashback on Axis Bank Credit
            Card <a class="text-primary text-weight-bolder">T&C</a></li>
          <li class="q-mt-xs"><span class="text-weight-bold">Bank Offer</span> 5% Unlimited Cashback on Axis Bank Credit
            Card <a class="text-primary text-weight-bolder">T&C</a></li>
          <li class="q-mt-xs"><span class="text-weight-bold">Bank Offer</span> OfferExtra 5% off* <a
            class="text-primary text-weight-bolder">T&C</a></li>
        </ul>
        <q-tabs
          v-model="tab"
          dense
          align="left"
          class="bg-primary text-white shadow-2"
          :breakpoint="0"
        >
          <q-tab name="Specifications" icon="info" label="Specifications"/>
          <q-tab name="Ratings & Reviews" icon="star" label="Ratings & Reviews"/>
        </q-tabs>
        <q-tab-panels style="border: 1px solid lightgrey" v-model="tab">
          <q-tab-panel name="Specifications">
            <q-list dense bordered class="rounded-borders" style="">
              <q-item-label class="text-grey-10" header>General</q-item-label>
              <q-item v-ripple>
                <q-item-section>
                  <div class="row">
                    <div class="col-3 text-grey-6">Dial Color</div>
                    <div class="col-9">Black</div>
                  </div>
                  <div class="row">
                    <div class="col-3 text-grey-7">Dial Color</div>
                    <div class="col-9">Black</div>
                  </div>
                  <div class="row">
                    <div class="col-3 text-grey-7">Strap Material</div>
                    <div class="col-9">Silicone</div>
                  </div>
                  <div class="row">
                    <div class="col-3 text-grey-7">Usage</div>
                    <div class="col-9">Fitness & Outdoor, Health & Medical, Notifier, Safety & Security, Watchphone
                    </div>
                  </div>

                </q-item-section>
              </q-item>
              <q-item-label header>Product Details</q-item-label>
              <q-item-label header>Camera And Display Features</q-item-label>
              <q-item-label header>Dimensions</q-item-label>
              <q-item-label header>Warranty</q-item-label>
              <q-item v-ripple>

                <!--<q-item-section>-->
                <q-item-label lines="1">6 months warranty</q-item-label>
                <!--</q-item-section>-->
              </q-item>
            </q-list>
          </q-tab-panel>


          <q-tab-panel name="Ratings & Reviews">
            <q-list bordered class="rounded-borders" style="">
              <q-item-label header>Reviews</q-item-label>

              <q-item v-ripple>
                <q-item-section avatar>
                  <q-avatar>
                    <img src="https://cdn.quasar.dev/img/avatar2.jpg">
                  </q-avatar>
                </q-item-section>

                <q-item-section>
                  <q-item-label lines="1">Brunch this weekend?</q-item-label>
                  <q-item-label caption lines="2">
                    <span class="text-weight-bold">Janet</span>
                    -- I'll be in your neighborhood doing errands this
                    weekend. Do you want to grab brunch?
                  </q-item-label>
                </q-item-section>

                <q-item-section side top>
                  1 min ago
                </q-item-section>
              </q-item>

              <q-separator inset="item"/>

              <q-item v-ripple>
                <q-item-section avatar>
                  <q-avatar>
                    <img src="https://cdn.quasar.dev/img/avatar4.jpg">
                  </q-avatar>
                </q-item-section>

                <q-item-section>
                  <q-item-label lines="1">Linear Project</q-item-label>
                  <q-item-label caption lines="2">
                    <span class="text-weight-bold">John</span>
                    -- Can we schedule a call for tomorrow?
                  </q-item-label>
                </q-item-section>

                <q-item-section side top>
                  1 min ago
                </q-item-section>
              </q-item>

              <q-separator inset="item"/>

              <q-item v-ripple>
                <q-item-section avatar>
                  <q-avatar>
                    <img src="https://cdn.quasar.dev/img/avatar2.jpg">
                  </q-avatar>
                </q-item-section>

                <q-item-section>
                  <q-item-label lines="1">Brunch this weekend?</q-item-label>
                  <q-item-label caption lines="2">
                    <span class="text-weight-bold">Janet</span>
                    -- I'll be in your neighborhood doing errands this
                    weekend. Do you want to grab brunch?
                  </q-item-label>
                </q-item-section>

                <q-item-section side top>
                  1 min ago
                </q-item-section>
              </q-item>

              <q-separator inset="item"/>

              <q-item v-ripple>
                <q-item-section avatar>
                  <q-avatar>
                    <img src="https://cdn.quasar.dev/img/avatar4.jpg">
                  </q-avatar>
                </q-item-section>

                <q-item-section>
                  <q-item-label lines="1">Linear Project</q-item-label>
                  <q-item-label caption lines="2">
                    <span class="text-weight-bold">John</span>
                    -- Can we schedule a call for tomorrow?
                  </q-item-label>
                </q-item-section>

                <q-item-section side top>
                  1 min ago
                </q-item-section>
              </q-item>
            </q-list>
          </q-tab-panel>
        </q-tab-panels>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "details.vue",
    data() {
      return {
        slide: 1,
        tab: 'Specifications'
      }
    }
  }
</script>

<style scoped>

</style>
