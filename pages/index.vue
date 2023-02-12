<template>
  <v-container style="">
    <v-row no-gutters>
      <v-col class="header">
        <v-card class="">
          <div class="text-overline test">ธุระกรรม</div>
          <v-btn
            style="width: 100%"
            outlined
            rounded
            text
            @click="$vuetify.theme.dark = !$vuetify.theme.dark"
          >
            โอนเงิน
          </v-btn>
          <v-btn
            style="width: 100%"
            outlined
            rounded
            text
            @click="$vuetify.theme.dark = !$vuetify.theme.dark"
          >
            ถอนเงิน
          </v-btn>
          <v-btn
            style="width: 100%"
            outlined
            rounded
            text
            @click="$vuetify.theme.dark = !$vuetify.theme.dark"
          >
            ฝากเงิน
          </v-btn>
        </v-card>
      </v-col>

      <v-col>
        <v-card>
          <v-card-text class="text-h5 font-weight-bold"> คงเหลือ: </v-card-text>
          <v-card-text>
            <!-- <v-img src="https://img.icons8.com/external-justicon-lineal-justicon/64/null/external-wallet-economy-and-currency-justicon-lineal-justicon.png" width="50"></v-img> -->
            <v-img
              src="https://img.icons8.com/external-kiranshastry-lineal-kiranshastry/64/null/external-wallet-interface-kiranshastry-lineal-kiranshastry.png"
              width="50"
            ></v-img>
            500 บาท
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
    <v-row>
      <v-data-table
        :headers="headers"
        :items="desserts"
        :items-per-page="5"
        style="width: 100%"
        class="elevation-1 mx-auto"
      ></v-data-table>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      headers: [
        {
          text: 'Dessert (100g serving)',
          align: 'start',
          sortable: false,
          value: 'name',
        },
        { text: 'Calories', value: 'calories' },
        { text: 'Fat (g)', value: 'fat' },
        { text: 'Carbs (g)', value: 'carbs' },
        { text: 'Protein (g)', value: 'protein' },
        { text: 'Iron (%)', value: 'iron' },
      ],
      desserts: [
        {
          name: 'Frozen Yogurt',
          calories: 159,
          fat: 6.0,
          carbs: 24,
          protein: 4.0,
          iron: 1,
        },
        {
          name: 'Ice cream sandwich',
          calories: 237,
          fat: 9.0,
          carbs: 37,
          protein: 4.3,
          iron: 1,
        },
        {
          name: 'Eclair',
          calories: 262,
          fat: 16.0,
          carbs: 23,
          protein: 6.0,
          iron: 7,
        },
        {
          name: 'Cupcake',
          calories: 305,
          fat: 3.7,
          carbs: 67,
          protein: 4.3,
          iron: 8,
        },
        {
          name: 'Gingerbread',
          calories: 356,
          fat: 16.0,
          carbs: 49,
          protein: 3.9,
          iron: 16,
        },
        {
          name: 'Jelly bean',
          calories: 375,
          fat: 0.0,
          carbs: 94,
          protein: 0.0,
          iron: 0,
        },
        {
          name: 'Lollipop',
          calories: 392,
          fat: 0.2,
          carbs: 98,
          protein: 0,
          iron: 2,
        },
        {
          name: 'Honeycomb',
          calories: 408,
          fat: 3.2,
          carbs: 87,
          protein: 6.5,
          iron: 45,
        },
        {
          name: 'Donut',
          calories: 452,
          fat: 25.0,
          carbs: 51,
          protein: 4.9,
          iron: 22,
        },
        {
          name: 'KitKat',
          calories: 518,
          fat: 26.0,
          carbs: 65,
          protein: 7,
          iron: 6,
        },
      ],
    }
  },
  mounted() {
    this.$vuetify.theme.dark = true
  },
}
</script>
<style lang="scss" scoped>
.test {
  background-color: aqua;
}
</style>
