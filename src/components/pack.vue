<template>
    <v-row justify="center" class="space px-16 mb-5">
        <v-col cols="12" xs="12" sm="6" md="4" v-for="(pack ,i ) in packs" :key="i">
        <v-card class="mx-auto rounded-xl" max-width="300" flat outlined>
            <div align="center" justify="center">
            <v-img max-height="300" max-width="300" :src="pack.img" contain ></v-img>
            </div>
              <v-card-title>
                {{pack.title}}
            </v-card-title>
            <v-card-title class="grey--text text-grey-darken-1 caption mt-n6">
                {{pack.subtitle}}
            </v-card-title>
            <v-card-title class="mt-n4">
                {{pack.price}}
            </v-card-title>
            <productCount></productCount>
            <!-- <v-card-actions class="mw-2 mt-n4">
                <v-btn outlined class="mt-n2 add" >
                    <v-icon color="green">
                        mdi-minus
                    </v-icon>
                </v-btn>
                <strong class="mx-2">
                    {{bpm}}
                </strong>
                 <v-btn outlined class="mt-n2 add"  >
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
        bpm: 0,
      packs: [
        {
          img: "p1.png",
          title: "Medium Box",
          subtitle: "Tomato, Cabbage, Oil, Cauliflower",
          price: "$55",
        },
        {
          img: "p2.png",
          title: "Big Pack",
          subtitle: "Tomato, Cabbage, Oil, Cauliflower",
          price: "$55",
        },
        {
          img: "p3.png",
          title: "Small",
          subtitle: "Tomato, Cabbage, Oil,Cauliflower ",
          price: "$55",
        },
        {
          img: "p4.png",
          title: "Medium Box",
          subtitle: "Tomato, Cabbage, Oil,Cauliflower",
          price: "$55",
        },
        {
          img: "p5.png",
          title: "Medium Box",
          subtitle: "Tomato, Cabbage, Oil,Cauliflower",
          price: "$55",
        },
        {
          img: "p6.png",
          title: "Medium Box",
          subtitle: "Tomato, Cabbage, Oil,Cauliflower",
          price: "$55",
        },
      ],
    };
  },
};
</script>

<style></style>
