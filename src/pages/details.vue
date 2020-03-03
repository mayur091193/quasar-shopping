<template>
  <div>
    <div class="row bg-white q-mt-sm">
      <div class="col-lg-5 col-md-5 col-sm-12 col-xs-12">
        <div class="q-pa-md">

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


        </div>
      </div>
      <div class="col-lg-7 col-md-7 col-sm-12 col-xs-12">
        <!--<q-scroll-area :style="{'height':(win_height-200)+'px'}">-->
        <div class="row">
          <div class="col-lg-7 col-md-7 col-sm-12 col-xs-12" :class="$q.platform.is.desktop ? '' : 'q-px-md'">
            <div class="text-subtitle1 text-grey-10 q-mt-sm q-pt-xs">Benling C200-BLK Smartwatch (Black Strap Free Size)
            </div>
            <div>
              <q-chip size="10px" class="text-weight-bold q-px-xs" square color="green-7" text-color="white"
                      icon-right="star">
                4.4
              </q-chip>
              <span class="text-caption text-weight-bold text-grey-6">6 Ratings & 2 Reviews</span>
            </div>
            <div>
              <div class="text-caption text-green-8 text-weight-bolder q-mt-sm">Special Price</div>
              <span class="text-h6">₹3,149</span><span class="q-ml-sm text-grey-6"
                                                       style="text-decoration: line-through">₹3,699</span>
              <span class="q-ml-md text-caption text-green-8 text-weight-bolder q-mt-md">20% off</span>
            </div>
            <div class="q-mt-sm text-weight-bold">
              Offers
              <ul class="q-pl-sm text-caption" style="list-style-type: none">
                <li class="q-mt-xs"><span class="text-weight-bold">Bank Offer</span> 5% Unlimited Cashback on Axis Bank
                  Credit
                  Card <a class="text-primary text-weight-bolder">T&C</a></li>
                <li class="q-mt-xs"><span class="text-weight-bold">Bank Offer</span> 5% Unlimited Cashback on Axis Bank
                  Credit
                  Card <a class="text-primary text-weight-bolder">T&C</a></li>
                <li class="q-mt-xs"><span class="text-weight-bold">Bank Offer</span> OfferExtra 5% off* <a
                  class="text-primary text-weight-bolder">T&C</a></li>
              </ul>
            </div>
            <div class="q-mt-sm">
              <div class="text-subtitle1 text-green-8 text-weight-bold">In stock.</div>
              <div class="text-caption q-mt-sm text-grey-8 text-weight-bold">Delivery by: <span class="text-black">Tue, Mar 3</span>
              </div>
              <div class="text-caption text-subtitle2 text-grey-8 text-weight-bold">Fastest delivery: <span
                class="text-black">Mon, Mar 2 by 9pm</span></div>
            </div>
            <div class="q-mt-md">
              <q-btn class="q-mt-md" color="orange-9" icon="shopping_cart" label="Add to cart"/>
              <q-btn class="q-mt-md q-ml-md" color="orange-8" icon="shopping_cart" label="Buy now"/>
            </div>
          </div>
          <div class="col-lg-5 col-md-5 col-sm-12 col-xs-12 q-mt-md q-pt-xs q-pl-lg">
            <div class="text-subtitle2">Customer rating</div>
            <div class="text-h3">4.2</div>
            <div>
              <q-rating
                v-model="rating_point"
                max="5"
                size="2em"
                color="orange"
                icon="star_border"
                icon-selected="star"
                icon-half="star_half"
                no-dimming
                readonly
              />
            </div>
            <div class="text-subtitle2 text-grey-8">(357 reviews)</div>
            <div class="text-subtitle2 text-grey-10 q-mt-sm">93% would recommend to a friend</div>

            <q-list dense bordered padding class="no-border q-mt-lg q-pr-xl">
              <q-item style="padding-left: 0 !important;" v-ripple>
                <span class="text-subtitle2 q-mr-xs">5</span>
                <q-icon name="star" size="1.5em" color="orange"></q-icon>
                <q-linear-progress class="q-ml-sm  q-mr-sm" style="margin-top: 5px;" size="13px" :value="0.9"/>
                <span style="margin-top: 2px" class="text-caption text-weight-bold text-grey-8">273</span>
              </q-item>
              <q-item style="padding-left: 0 !important;" v-ripple>
                <span class="text-subtitle2 q-mr-xs">4</span>
                <q-icon name="star" size="1.5em" color="orange"></q-icon>
                <q-linear-progress class="q-ml-sm  q-mr-sm" style="margin-top: 5px;" size="13px" :value="0.6"/>
                <span style="margin-top: 2px" class="text-caption text-weight-bold text-grey-8">&nbsp;&nbsp;69</span>
              </q-item>
              <q-item style="padding-left: 0 !important;" v-ripple>
                <span class="text-subtitle2 q-mr-xs">3</span>
                <q-icon name="star" size="1.5em" color="orange"></q-icon>
                <q-linear-progress class="q-ml-sm  q-mr-sm" style="margin-top: 5px;" size="13px" :value="0.1"/>
                <span style="margin-top: 2px" class="text-caption text-weight-bold text-grey-8">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;6</span>
              </q-item>
              <q-item style="padding-left: 0 !important;" v-ripple>
                <span class="text-subtitle2 q-mr-xs">2</span>
                <q-icon name="star" size="1.5em" color="orange"></q-icon>
                <q-linear-progress class="q-ml-sm  q-mr-sm" style="margin-top: 5px;" size="13px" :value="0.1"/>
                <span style="margin-top: 2px" class="text-caption text-weight-bold text-grey-8">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3</span>
              </q-item>
              <q-item style="padding-left: 0 !important;" v-ripple>
                <span class="text-subtitle2 q-mr-xs">1</span>
                <q-icon name="star" size="1.5em" color="orange"></q-icon>
                <q-linear-progress class="q-ml-sm  q-mr-sm" style="margin-top: 5px;" size="13px" :value="0.1"/>
                <span style="margin-top: 2px" class="text-caption text-weight-bold text-grey-8">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;6</span>
              </q-item>

            </q-list>
          </div>
        </div>

        <!--</q-scroll-area>-->
      </div>
    </div>
    <div class="row q-mt-sm">
      <div class="col-lg-12 col-md-12 col-sm-12 col-xs-12">
        <q-tabs
          v-model="tab"
          dense
          align="left"
          class="bg-primary text-white shadow-2"
          :breakpoint="0"
        >
          <q-tab name="Specifications" label="Specifications"/>
          <q-tab name="Ratings & Reviews" label="Ratings & Reviews"/>
          <q-tab name="Similar products" label="Similar products"/>
          <q-tab name="Bought together" label="Bought together"/>
          <q-tab name="Recently Viewed" label="Recently Viewed"/>
        </q-tabs>
        <q-tab-panels style="border: 1px solid lightgrey" v-model="tab">
          <q-tab-panel name="Specifications">
            <div class="row">
              <div class="col-lg-4 col-md-4 col-sm-12 col-xs-12">
                <q-list bordered class="rounded-borders" style="">
                  <q-item-label class="text-weight-bolder" header>General</q-item-label>
                  <q-item>
                    <q-item-section>
                      <span class="text-caption text-grey">Dial Color</span>
                      <span>Black</span>
                    </q-item-section>
                    <q-item-section>
                      <span class="text-caption text-grey">Strap Material</span>
                      <span>Silicone</span>
                    </q-item-section>
                  </q-item>
                  <q-item>
                    <q-item-section>
                      <span class="text-caption text-grey">Usage</span>
                      <span>Fitness & Outdoor, Health & Medical, Notifier, Safety & Security, Watchphone</span>
                    </q-item-section>
                  </q-item>
                </q-list>
              </div>
              <div class="col-lg-4 col-md-4 col-sm-12 col-xs-12">
                <q-list bordered class="rounded-borders" style="">
                  <q-item-label class="text-weight-bolder" header>Product Details</q-item-label>
                  <q-item>
                    <q-item-section>
                      <span class="text-caption text-grey">Dial Color</span>
                      <span>Black</span>
                    </q-item-section>
                    <q-item-section>
                      <span class="text-caption text-grey">Strap Material</span>
                      <span>Silicone</span>
                    </q-item-section>
                  </q-item>
                </q-list>
              </div>
              <div class="col-lg-4 col-md-4 col-sm-12 col-xs-12">
                <q-list bordered class="rounded-borders" style="">
                  <q-item-label class="text-weight-bolder" header>Camera And Display Features</q-item-label>
                  <q-item>
                    <q-item-section>
                      <span class="text-caption text-grey">Dial Color</span>
                      <span>Black</span>
                    </q-item-section>
                    <q-item-section>
                      <span class="text-caption text-grey">Strap Material</span>
                      <span>Silicone</span>
                    </q-item-section>
                  </q-item>
                </q-list>
              </div>
            </div>
            <!--<q-list dense bordered class="rounded-borders" style="">-->
            <!--<q-item-label class="text-grey-10" header>General</q-item-label>-->
            <!--<q-item v-ripple>-->
            <!--<q-item-section>-->
            <!--<div class="row">-->
            <!--<div class="col-3 text-grey-6">Dial Color</div>-->
            <!--<div class="col-9">Black</div>-->
            <!--</div>-->
            <!--<div class="row">-->
            <!--<div class="col-3 text-grey-7">Dial Color</div>-->
            <!--<div class="col-9">Black</div>-->
            <!--</div>-->
            <!--<div class="row">-->
            <!--<div class="col-3 text-grey-7">Strap Material</div>-->
            <!--<div class="col-9">Silicone</div>-->
            <!--</div>-->
            <!--<div class="row">-->
            <!--<div class="col-3 text-grey-7">Usage</div>-->
            <!--<div class="col-9">Fitness & Outdoor, Health & Medical, Notifier, Safety & Security, Watchphone-->
            <!--</div>-->
            <!--</div>-->

            <!--</q-item-section>-->
            <!--</q-item>-->
            <!--<q-item-label header>Product Details</q-item-label>-->
            <!--<q-item-label header>Camera And Display Features</q-item-label>-->
            <!--<q-item-label header>Dimensions</q-item-label>-->
            <!--<q-item-label header>Warranty</q-item-label>-->
            <!--<q-item v-ripple>-->

            <!--&lt;!&ndash;<q-item-section>&ndash;&gt;-->
            <!--<q-item-label lines="1">6 months warranty</q-item-label>-->
            <!--&lt;!&ndash;</q-item-section>&ndash;&gt;-->
            <!--</q-item>-->
            <!--</q-list>-->
          </q-tab-panel>


          <q-tab-panel name="Ratings & Reviews">
            <div class="row">
              <div class="col-lg-6 col-md-6 col-sm-12 col-xs-12">
                <q-list bordered class="rounded-borders" style="">
                  <q-item-label class="text-weight-bolder text-green-8" header>Positive Reviews</q-item-label>

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
              </div>
              <div class="col-lg-6 col-md-6 col-sm-12 col-xs-12">
                <q-list bordered class="rounded-borders" style="">
                  <q-item-label class="text-weight-bolder text-red-8" header>Negative Reviews</q-item-label>

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
              </div>
            </div>

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
        tab: 'Specifications',
        rating_point: 4.3,
        rat_5: 5,
        rat_4: 4,
        rat_3: 3,
        rat_2: 2,
        rat_1: 1,
      }
    },
    computed: {
      win_width() {
        return this.$q.screen.width - 59;
      },
      win_height() {
        return this.$q.screen.height - 0;
      }
    }
  }
</script>

<style scoped>

</style>
