<template>
  <q-layout>
    <q-page-container>
      <q-page class="flex flex-center" style="font-family: Lato;">
        <div id="particles-js"></div>
        <q-card class="row my-card items-center q-pa-none q-ma-none shadow-24">
          <q-card-section class="col-4 items-center float-left" style="background-color: #1f509e"
                          :style="{'height':(win_height-270)+'px'}" horizontal>
            <div class="text-center full-width">
              <div class="text-weight-bolder text-white text-h6">Quasar Shopping</div>
              <div class="text-caption text-white">Quasar Shopping - One stop solution</div>
            </div>
          </q-card-section>
          <q-card-section class="col-8 float-left">
            <q-card-section class="items-center">
              <div>

                <q-form style="width: 50%;margin: auto;" class="q-gutter-md">
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
                  <div>
                    <q-btn dense label="Login" to="/dashboard" type="button" color="primary"/>
                  </div>
                </q-form>

              </div>
            </q-card-section>
          </q-card-section>


        </q-card>
        <!--        <q-card class="login-form" v-bind:style="$q.platform.is.mobile?{'width': '80%'}:{'width':'30%'}">-->
        <!--          <q-img src="/statics/images/shop.jpg"></q-img>-->
        <!--          <q-card-section>-->
        <!--            <q-avatar size="74px" class="absolute" style="top: 0;right: 25px;transform: translateY(-50%);">-->
        <!--              <img src="https://cdn.quasar.dev/img/boy-avatar.png">-->
        <!--            </q-avatar>-->
        <!--            <div class="row no-wrap items-center">-->
        <!--              <div class="col text-h6 ellipsis">-->
        <!--                Log in to Dashboard-->
        <!--              </div>-->
        <!--            </div>-->
        <!--          </q-card-section>-->
        <!--          <q-card-section>-->
        <!--            <q-form-->
        <!--              class="q-gutter-md"-->
        <!--            >-->
        <!--              <q-input-->
        <!--                filled-->
        <!--                v-model="username"-->
        <!--                label="Username"-->
        <!--                lazy-rules-->
        <!--              />-->

        <!--              <q-input-->
        <!--                type="password"-->
        <!--                filled-->
        <!--                v-model="password"-->
        <!--                label="Password"-->
        <!--                lazy-rules-->

        <!--              />-->

        <!--              <div>-->
        <!--                <q-btn label="Login" to="/dashboard" type="button" color="primary"/>-->
        <!--              </div>-->
        <!--            </q-form>-->
        <!--          </q-card-section>-->
        <!--        </q-card>-->
      </q-page>
    </q-page-container>
  </q-layout>
</template>

<script>
    export default {
        data() {
            return {
                username: 'admin',
                password: 'Admin@CRM'
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
