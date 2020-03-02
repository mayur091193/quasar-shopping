<template>
  <div>
    <div class="row bg-white q-mt-sm">
      <div class="col-2" style="border-right: 1px solid lightgrey">
        <q-card class="q-mr-sm no-shadow">
          <!--<q-card-section class="text-subtitle1 text-grey-8">-->
          <!--Filter By-->
          <!--</q-card-section>-->
          <transition-group
            appear
            enter-active-class="animated fadeInLeft"
          >
            <q-list v-for="item in filters_list" :key="item.label">
              <q-item-label class="text-weight-bolder text-grey-9 q-pt-md q-pb-sm" header>{{item.label}}</q-item-label>
              <q-item class="q-pa-none" v-for="it in item.items" :key="it.model" tag="label" v-ripple dense>
                <q-item-section side class="q-px-md text-caption">
                  <q-checkbox @input="searched_results=[],show_load_more=false,log_offset=0,do_search()" dense
                              v-model="it[it.model]">
                    {{it.label}}({{it.count}})
                  </q-checkbox>
                </q-item-section>
              </q-item>
              <q-item class="q-py-none text-weight-bold text-indigo text-caption cursor-pointer"
                      style="min-height: 10px">
                View All
              </q-item>
            </q-list>
          </transition-group>
        </q-card>
      </div>
      <div class="col-10">
        <div class="q-pa-md row items-start q-gutter-md">
          <q-card @click="$router.push('/details')" class="cursor-pointer" :class="class_val"
                  @mouseover="class_val='my-card shadow-20'"
                  @mouseleave="class_val='my-card shadow-'">
            <q-img src="https://cdn.quasar.dev/img/chicken-salad.jpg"></q-img>

            <q-card-section class="q-pb-xs q-pt-md">
              <!--<q-btn-->
              <!--fab-->
              <!--color="primary"-->
              <!--icon="shopping_cart"-->
              <!--class="absolute"-->
              <!--style="top: 0; right: 12px; transform: translateY(-50%);"-->
              <!--&gt;</q-btn>-->

              <div class="row no-wrap items-center">
                <div class="col text-subtitle2 ellipsis-2-lines text-grey-10">
                  Benling C200-BLK Smartwatch (Black Strap Free Size)
                </div>
                <div class="col-auto text-grey text-caption q-pt-md row no-wrap items-center">
                  <!--<q-icon name="place"></q-icon>-->
                  <!--250 ft-->
                </div>
              </div>

              <q-rating v-model="stars" color="orange" :max="5" readonly size="17px"></q-rating>
            </q-card-section>

            <q-card-section class="q-py-sm">
              <div>
                <div class="text-caption text-green-8 text-weight-bolder">Special Price</div>
                <span class="text-h6">₹3,149</span><span class="q-ml-sm text-grey-6"
                                                         style="text-decoration: line-through">₹3,699</span>
                <span class="q-ml-md text-caption text-green-8 text-weight-bolder q-mt-md">20% off</span>
              </div>
              <!--<div class="text-subtitle1">-->
              <!--$・Italian, Cafe-->
              <!--</div>-->
              <!--<div class="text-caption text-grey">-->
              <!--Small plates, salads & sandwiches in an intimate setting.-->
              <!--</div>-->
            </q-card-section>

            <q-separator></q-separator>

            <q-card-actions>
              <q-btn flat class="text-weight-bold text-capitalize" dense color="primary">
                View details
              </q-btn>
            </q-card-actions>
          </q-card>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "category.vue",
    data() {
      return {
        stars: 4,
        class_val: "shadow-1 my-card",
        filters_list: [
          {
            "label": "Product",
            "items": [
              {
                "Product": false,
                "count": 51,
                "label": "Wealth Management",
                "model": "Product"
              },
              {
                "Product": false,
                "count": 3,
                "label": "Brokerage",
                "model": "Product"
              },
              {
                "Product": false,
                "count": 41,
                "label": "Strategic Investment",
                "model": "Product"
              },
              {
                "Product": false,
                "count": 16,
                "label": "Investment Banking",
                "model": "Product"
              }
            ]
          },
          {
            "label": "Asset Type",
            "items": [
              {
                "AssetType": false,
                "count": 51,
                "label": "Print Ad",
                "model": "AssetType"
              },
              {
                "AssetType": false,
                "count": 3,
                "label": "Standee",
                "model": "AssetType"
              },
              {
                "AssetType": false,
                "count": 23,
                "label": "Backdrop",
                "model": "AssetType"
              },
              {
                "AssetType": false,
                "count": 65,
                "label": "Hoarding",
                "model": "AssetType"
              },
              {
                "AssetType": false,
                "count": 35,
                "label": "Brochure",
                "model": "AssetType"
              },
              {
                "AssetType": false,
                "count": 23,
                "label": "Flyer",
                "model": "AssetType"
              },
              {
                "AssetType": false,
                "count": 12,
                "label": "Conference Material",
                "model": "AssetType"
              }
            ]
          },
          {
            "label": "Period",
            "items": [
              {
                "Period": false,
                "count": 51,
                "label": "2020",
                "model": "Period"
              },
              {
                "Period": false,
                "count": 3,
                "label": "2019",
                "model": "Period"
              },
              {
                "Period": false,
                "count": 23,
                "label": "2018",
                "model": "Period"
              },
              {
                "Period": false,
                "count": 65,
                "label": "2017",
                "model": "Period"
              }
            ]
          },
          {
            "label": "Language",
            "items": [
              {
                "Language": false,
                "count": 51,
                "label": "English",
                "model": "Language"
              },
              {
                "Language": false,
                "count": 3,
                "label": "Hindi",
                "model": "Language"
              },
              {
                "Language": false,
                "count": 23,
                "label": "Marathi",
                "model": "Language"
              },
              {
                "Language": false,
                "count": 65,
                "label": "Gujarati",
                "model": "Language"
              }
            ]
          }
        ]
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
  .my-card {
    width: 100%;
    max-width: 300px;
  }
</style>
