<template>
  <q-page class="main-container">
    <q-img src="../assets/flight.jpg" height="500px">
      <div class="absolute-center breadcrumb text-center">
        <p class="text-h4 text-uppercase">About</p>
        <span>Elements > Flight Top Filter</span>
      </div>
    </q-img>
    <div class="row justify-center">
      <div class="col-9 q-my-xl">
        <div v-if="$q.screen.gt.sm">
          <q-card flat class="q-pa-md">
            <div class="row q-py-md">
              <div class="col-2">
                <div class="label-style">From</div>
                <div class="input-box">
                  <q-input square outlined dense placeholder="From">
                    <template v-slot:append>
                      <q-img src="../assets/from.png" class="from-icon" />
                    </template>
                  </q-input>
                </div>
              </div>
              <div class="col-2">
                <div class="label-style">To</div>
                <div class="input-box">
                  <q-input square outlined dense placeholder="To">
                    <template v-slot:append>
                      <q-icon name="mdi-map-marker-outline" class="from-icon" size="xs" />
                    </template>
                  </q-input>
                </div>
              </div>
              <div class="col-2">
                <div class="label-style">Departure Date</div>
                <div class="input-box">
                  <q-input square outlined dense placeholder="Depart Date">
                    <template v-slot:append>
                      <q-icon name="event" class="from-icon" size="xs" />
                    </template>
                  </q-input>
                </div>
              </div>
              <div class="col-2">
                <div class="label-style">Return Date</div>
                <div class="input-box">
                  <q-input square outlined dense placeholder="Return Date">
                    <template v-slot:append>
                      <q-icon name="event" class="from-icon" size="xs" />
                    </template>
                  </q-input>
                </div>
              </div>
              <div class="col-2">
                <div class="label-style">Traveller & Class</div>
                <div class="input-box">
                  <q-input square outlined dense placeholder="To">
                    <template v-slot:append>
                      <q-icon name="mdi-account" class="from-icon" size="xs" />
                    </template>
                  </q-input>
                </div>
              </div>
              <div class="col-2">
                <q-btn
                  unelevated
                  @mouseenter="mouseOn = true"
                  @mouseleave="mouseOn = false"
                  :outline="mouseOn ?true: false"
                  :color="mouseOn ? 'primary' : ''"
                  label="Search"
                  class="search-btn text-weight-bold"
                  style="font-size: 16px; letter-spacing: 0.10em"
                />
              </div>
            </div>
          </q-card>
        </div>
        <div v-else></div>
      </div>
    </div>
  </q-page>
</template>

<script>
export default {
  name: "PageIndex",
  data() {
    return {
      mouseOn: false
    };
  }
};
</script>
<style lang="scss">
.main-container {
  background: #fafafa;
}
.breadcrumb {
  background: rgba(255, 255, 255, 0.6) !important;
  color: #4291b8 !important;
  padding: 31px 72px !important;
  p {
    margin: -2px 0px 16px;
    font-size: calc(18px + (36 - 18) * ((100vw - 320px) / (1920 - 320)));
    font-weight: 800;
  }
  span {
    color: black;
    font-size: calc(14px + (18 - 14) * ((100vw - 320px) / (1920 - 320)));
    font-weight: 700;
  }
}
.input-box {
  width: 85%;
  .q-field__append {
    border-left: 1px solid #e5e5e5;
  }
}
.from-icon {
  width: 15px;
  color: #e5e5e5;
}
.label-style {
  text-transform: capitalize;
  margin-bottom: 5px;
  font-weight: 700;
  font-size: 15px;
}
.search-btn {
  background: rgb(66, 145, 184);
  border-radius: 0px;
  position: relative;
  top: 20px;
  width: 92%;
}
</style>
