<template>
  <v-container
    fill-height
    :class="{ 'm-h-80vh': $vuetify.breakpoint.mdAndUp }"
    style="overflow-y: hidden;"
  >
    <v-row justify="space-around" align="center">
      <v-col cols="12" md="6" lg="4">
        <div>
          <div :class="{ 'text-center': $vuetify.breakpoint.smAndDown }">
            <h1
              class="text-h3 font-weight-bold primary--text"
              style="line-height: 1.4"
            >
              我们提供可满足
              <br />
              各种需求的现代 Vue 模板
            </h1>

            <p class="my-6 subtitle-1">
              使用 Vuetify，Ant Design Vue 等 UI 库构建的易于定制的现代 Vue UI
              模板和组件。
              所有的组件都是模块化且完全符合响应式的，不用担心各种设备上的兼容性的问题。
            </p>
          </div>

          <div>
            <v-row>
              <v-col cols="6" v-for="item in feature" :key="item.text">
                <v-icon color="primary">
                  mdi-check-circle-outline
                </v-icon>

                {{ item.text }}
              </v-col>
            </v-row>
          </div>
        </div>
      </v-col>

      <v-col cols="12" md="6">
        <v-row
          class="card-scroll"
          :class="{ 'm-h-80vh': $vuetify.breakpoint.mdAndUp }"
        >
          <v-col v-for="item in theme" :key="item.text" xl="6">
            <v-card hover :href="item.href">
              <v-img :src="item.img" />
              <v-card-title>
                {{ item.text }}
              </v-card-title>
            </v-card>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "HelloWorld",

  data: () => ({
    feature: [
      {
        text: "3 个完整应用程序模板"
      },
      {
        text: "20+ 单个页面"
      },
      {
        text: "50+ 组件"
      },
      {
        text: "使用多种 UI 库"
      },
      {
        text: "完全响应式"
      },
      {
        text: "可深度定制化"
      }
    ],
    theme: [
      {
        text: "Giraffe",
        img: require("../assets/giraffe.png"),
        href: "https://giraffe.heroui.net/"
      },
      {
        text: "Agency",
        img: require("../assets/agency.jpg"),
        href: "https://agency.heroui.net/"
      },
      {
        text: "Shock",
        img: require("../assets/shock.png"),
        href: "https://shock.heroui.net/"
      }
    ]
  })
};
</script>

<style lang="scss" scoped>
$small: 960px;

.m-h-80vh {
  max-height: 80vh;
}
.card-scroll {
  overflow: hidden;
  &:hover {
    @media screen and (min-width: $small) {
      overflow-y: scroll;
    }
  }
}
</style>
