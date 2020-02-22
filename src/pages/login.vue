<template>
  <q-layout>
    <q-page-container>
      <q-page class="flex flex-center" style="font-family: Lato;">
        <div id="particles-js"></div>
        <q-card class="row my-card items-center q-pa-none q-ma-none shadow-24">
          <q-card-section class="col-4 items-center float-left" style="background-color: #1f509e"
                          :style="{'height':(win_height-270)+'px'}" horizontal>
            <div class="text-center full-width">
              <div><img src="statics/images/logo.png" style="width: 33%"/></div>
              <div class="text-weight-bolder text-white text-h6">Quasar Shopping</div>
              <div class="text-caption text-white">Quasar Shopping - One stop solution</div>
            </div>
          </q-card-section>
          <q-card-section class="col-8 float-left">
            <q-card-section class="items-center">
              <div>

                <q-form style="width: 50%;margin: auto;" class="q-gutter-md">
                  <span class="text-subtitle1 text-weight-bold text-grey-7">Welcome Aboard</span>
                  <q-input
                    dense
                    outlined
                    v-model="username"
                    label="Username"
                    lazy-rules
                  />

                  <q-input
                    dense
                    type="password"
                    outlined
                    v-model="password"
                    label="Password"
                    lazy-rules
                  />
                  <q-checkbox class="text-grey-8" dense v-model="remember_me" label="Remember me"/>
                  <div>
                    <q-btn class="text-capitalize" size="sm" style="width:75px" dense label="Login" to="/home" type="button"
                           color="primary"/>
                    <q-btn class="float-right text-blue-9 text-capitalize" size="sm" style="width:75px;border: 1px solid #36669e;" dense label="Sign Up"
                           type="button"/>
                  </div>
                </q-form>

              </div>
            </q-card-section>
          </q-card-section>

        </q-card>
      </q-page>
    </q-page-container>
  </q-layout>
</template>

<script>
    export default {
        data() {
            return {
                username: 'admin',
                password: 'Admin@CRM',
                remember_me: false
            }
        },
        mounted() {

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
<style>
  .my-card {
    width: 55%;
    height: 30%;
  }

  #particles-js {
    position: absolute;
    width: 100%;
    height: 100%;
    /*background: linear-gradient(145deg, #abbaab 15%, #ffffff 70%);*/
    /*background: linear-gradient(145deg,#f7f8f8 11%, #627e79 75%);*/
    background-repeat: no-repeat;
    background-size: cover;
    background-position: 50% 50%;
  }

  .login-form {
    position: absolute;
  }
</style>
