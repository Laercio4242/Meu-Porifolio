<template>
  <section id="items">
    <v-parallax
      class="col-12"
      :height="$vuetify.breakpoint.smAndDown ? 700 : 500"
      src="https://cdn.pixabay.com/photo/2016/04/04/14/12/monitor-1307227_960_720.jpg"
    >
      <v-container fill-height class="col-12">
        <v-row class="mx-auto">
          <v-col v-for="(item, i) in items" :key="i">
            <div class="text-center" style="margin-left: -867px; margin-top: 240px;">
              <div class="display-3 font-weight-black mb-4">
                <img
                  class="img-logo" style="background: white;"
                  :src="require(`../assets/icons/${item.logo}`)"
                />
              </div>

              <div class="title font-weight-regular text-uppercase">
                {{ item.text }}
              </div>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </v-parallax>
  </section>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          logo: "js.svg",
          text: "Javascript",
        },
        // {
        //   logo: "html.svg",
        //   text: "HTML5",
        // },
        // {
        //   logo: "css.svg",
        //   text: "CSS3",
        // },
      ],
    };
  },
};
</script>

<style>
.img-logo {
  width: 70px;
}
</style>