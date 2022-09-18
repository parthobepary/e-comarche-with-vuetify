<template lang="">
  <div class="mt-10">
    <div>
      <template>
        <v-container fluid>
          <v-row>
            <v-col cols="12 shorted" md="3">
              <div class="stiky mt-16">
                <button class="secondary px-10 py-2 rounded mb-5">
                  Heigher price
                </button>
                <button class="secondary px-10 py-2 rounded mb-5">
                  Lower price
                </button>
                <button class="secondary px-10 py-2 rounded mb-5">
                  Best rated products</button
                ><button class="secondary px-10 py-2 rounded mb-5">
                  Low rated products
                </button>
              </div>
            </v-col>
            <v-col cols="12" md="9">
              <template>
                <v-container class="grey lighten-5">
                  <v-row no-gutters>
                    <v-col
                      v-for="(item, index) in shortedData"
                      :key="index"
                      cols="12"
                      sm="4"
                    >
                      <v-card
                        class="pa-2 ma-2 rounded-lg"
                        outlined
                        tile
                        height="350px"
                      >
                        <div class="title">
                          <p>
                            {{
                              item.title.length <= 50
                                ? item.title
                                : item.title.slice(20) + "..."
                            }}
                          </p>
                        </div>
                        <v-img
                          max-height="150"
                          max-width="250"
                          :src="item.image"
                        ></v-img>
                        <v-btn class="mt-5" color="success" width="100%">
                          Add to cards
                        </v-btn>
                      </v-card>
                    </v-col>
                  </v-row>
                </v-container>
              </template>
            </v-col>
          </v-row>
        </v-container>
      </template>
    </div>
  </div>
</template>
<script>
export default {
  name: "AllProducts",
  data() {
    return {
      allData: [],
      shortedData: [],
    };
  },
  mounted() {
    this.axios.get("https://fakestoreapi.com/products").then((res) => {
      this.allData = res.data;
      this.shortedData = [...this.allData];
    });
  },
};
</script>
<style lang="scss">
.title {
  height: 100px;
  background: yellow;
  margin-bottom: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.shorted {
  background-color: #cae8ca;
  border: 2px solid #4caf50;
}
.stiky {
  position: -webkit-sticky;
  position: sticky;
  top: 0;
  padding: 5px;
}
</style>
