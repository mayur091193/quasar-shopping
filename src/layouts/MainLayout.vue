<template>
  <q-layout view="lHh LpR lFf" style="font-family: Lato;">
    <q-header reveal elevated style="background-color: #1f509e;">
      <q-toolbar class="q-py-sm">
        <!--          <q-btn @click="left = !left" flat round dense icon="menu" class="q-mr-sm" />-->
        <img src="statics/images/logo.png" style="width: 3%"/>
        <q-toolbar-title>
          <span class="float-left q-mt-xs">Quasar Shopping</span>
        <q-input class="float-left q-ml-xl" style="width: 650px;" square bg-color="white" dense outlined v-model="text"
                 label="Search for products, brands and more"/>
          </q-toolbar-title>

        <q-btn flat round dense icon="settings" class="q-mr-md"/>
        <q-btn flat round dense icon="fas fa-sign-out-alt" to="/"/>
      </q-toolbar>
      <div class="bg-white text-grey-9 text-weight-bold shadow-transition">
        <div class="row text-center items-center" style="height: 38px">
          <div class="col-2 cursor-pointer hover-blue">
            Category 1
            <q-icon size="sm" class="q-ml-xs text-grey-5" name="keyboard_arrow_down"></q-icon>
          </div>
          <div class="col-2 cursor-pointer hover-blue">
            Category 2
            <q-icon size="sm" class="q-ml-xs text-grey-5" name="keyboard_arrow_down"></q-icon>
          </div>
          <div class="col-2 cursor-pointer hover-blue">
            Category 3
            <q-icon size="sm" class="q-ml-xs text-grey-5" name="keyboard_arrow_down"></q-icon>
          </div>
          <div class="col-2 cursor-pointer hover-blue">
            Category 4
            <q-icon size="sm" class="q-ml-xs text-grey-5" name="keyboard_arrow_down"></q-icon>
          </div>
          <div class="col-2 cursor-pointer hover-blue">
            Category 5
            <q-icon size="sm" class="q-ml-xs text-grey-5" name="keyboard_arrow_down"></q-icon>
          </div>
          <div class="col-2 cursor-pointer hover-blue">
            Category 6
            <q-icon size="sm" class="q-ml-xs text-grey-5" name="keyboard_arrow_down"></q-icon>
          </div>
        </div>
      </div>
    </q-header>


    <q-page-container style="background-color:#f1f2f6">
      <router-view/>
    </q-page-container>


  </q-layout>
</template>

<script>
    export default {
        data() {
            return {
                left: false
            }
        }
    }
</script>

<style>
  .q-drawer {
    /*background-image: url(https://demos.creative-tim.com/vue-material-dashboard/img/sidebar-2.32103624.jpg) !important;*/
    background-image: url('/statics/images/lake.jpg') !important;
    background-size: cover !important;
  }

  .q-drawer__content {
    background-color: rgba(1, 1, 1, 0.75);
  }

  .navigation-item {
    border-radius: 5px;
  }

  .tab-active {
    background-color: green;
  }

  .hover-blue:hover {
    color: #1f509e;
  }
</style>
