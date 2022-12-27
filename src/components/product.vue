<template>
  <v-row class="px-16 space" justify="center">
    <v-col cols="12" xs="12" sm="6" md="4" v-for="(product, i) in products" :key="i">
        <v-card class="mx-auto rounded-xl" max-width="300" flat outlined>
            <div align="center" justify="center">
            <v-img max-height="300" max-width="300" :src="product.img" contain ></v-img>
            </div>
            <v-card-title>
                {{product.title}}
            </v-card-title>
            <v-card-title class="grey--text text-grey-darken-1 caption mt-n6">
                {{product.subtitle}}
            </v-card-title>
            <v-card-title class="mt-n4">
                {{product.price}}
            </v-card-title>
            <productCount></productCount>
            <!-- <v-card-actions class="mw-2 mt-n4">
                <v-btn outlined class="mt-n2 add"  @click="decrement(i)">
                    <v-icon color="green">
                        mdi-minus
                    </v-icon>
                </v-btn>
                <strong class="mx-2">
                    {{bpm}}
                </strong>
                 <v-btn outlined class="mt-n2 add"  @click="increment">
                    <v-icon color="green">
                        mdi-plus
                    </v-icon>
                </v-btn>
                <v-spacer></v-spacer>
                <v-btn class="mx-2 mt-n3" fab dark small color="green">
                  <v-icon>
                    mdi-shopping
                  </v-icon>
                </v-btn>
            </v-card-actions> -->
        </v-card>
    </v-col>
  </v-row>
</template>

<script>
import productCount from './productCount.vue'
export default {
  components: {
    productCount
  },
  data() {
    return {
      bpm: 1,
      products: [
        { img: "pr1.png",
          title: "Cabbage",
          subtitle: "1kg",
          price: "$13" ,
          id: 1},
        {
          img: "pr2.png",
          title: "Perry's Ice Cream",
          subtitle: "1kg",
          price: "$23",
          id: 2
        },
        { img: "pr3.png", title: "Potato", subtitle: "1kg", price: "$17" },
        {
          img: "pr4.png",
          title: "Bundle Pack",
          subtitle: "Potato, Papaya, Oil, Cabbage",
          price: "$40",
          id: 3
        },
        {
          img: "pr5.png",
          title: "Oreo Biscuit",
          subtitle: "270GM",
          price: "$20",
          id: 4
        },
        { img: "pr6.png", title: "Papaya", subtitle: "1kg", price: "$10", id: 5 },
      ],
    };
  },
  methods: {
    // decrement (num) {
    //     this.bpm--

    //     // this.bpm = num    
    //     // console.log(num);

    // },
    // increment () {
    //   this.bpm++
    // } 
  }
};
</script>

<style></style>
