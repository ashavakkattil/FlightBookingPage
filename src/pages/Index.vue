<template>
  <q-page class="main-container">
    <q-img src="../assets/flight.jpg" height="500px">
      <div class="absolute-center breadcrumb text-center">
        <p class="text-h4 text-uppercase">About</p>
        <span>Elements > Flight Top Filter</span>
      </div>
    </q-img>
  </q-page>
</template>

<script>
export default {
  name: "PageIndex"
};
</script>
<style lang="scss" scoped>
.main-container {
  background: #fafafa;
}
.breadcrumb {
  background: rgba(255, 255, 255, 0.6);
  color: #4291b8;
  padding: 31px 72px;
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
</style>
