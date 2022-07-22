<template>
  <v-container fluid>
    <v-card color="#3853D8" height="150px" tile flat class="d-flex align-center justify-center" dark>
      <v-row>
        <v-col cols="12" sm="12">
          <h4 class="text-center">MEN'S LIFESTYLE SHOES</h4>
        </v-col>
        <v-col cols="12" sm="12">
          <v-breadcrumbs :items="items" class="justify-center mt-n7" dark>
            <template v-slot:divider>
              <v-icon color="#7C92FE">mdi-chevron-right</v-icon>
            </template>
          </v-breadcrumbs>
        </v-col>
      </v-row>
    </v-card>
    <v-card tile class="mx-16 mt-n10 card1" color="white">
      <v-row>
        <v-col cols="12" sm="8" class="pr-0">
          <v-card height="250px" tile flat color="#3890D8">
            <v-row>
              <v-col cols="12" sm="4" class="pl-8 pt-5">
                <v-btn color="black" dark class="withoutupercase" small tile>
                  NEW
                </v-btn>
                <h6 class="white--text mt-8">MOUNTAIN BIKE</h6>
                <h3 class="white--text mt-5">Trek Speed Concept</h3>
                <v-btn rounded color="#4C9CDB" dark class="withoutuperecase px-8 mt-10">
                  More info
                </v-btn>
              </v-col>
              <v-col cols="12" sm="8">
                <v-img src="/assets/images/bike.png" max-height="400" max-width="400" contain class="mt-n4"></v-img>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
        <v-col cols="12" sm="4" class="pl-0">
          <v-card height="250px" tile flat color="#6857E1">
            <v-row>
              <v-col cols="12" sm="6" class="pl-8 pt-5">
                <v-btn color="black" dark class="withoutipercase" small tile>
                  New
                </v-btn>
                <h6 class="white--text mt-8">DOWN JACKET</h6>
                <h3 class="white--text mt-5">Sale Collection 2022</h3>
                <v-btn rounded color="#8375E7" dark class="withoutupercase px-8 mt-3">
                  More Info 
                </v-btn>
              </v-col>
              <v-col cols="12" sm="6">
                <v-img src="/assets/images/jacket.png" max-height="400" max-width="420" contain class="mt-n2 mr-3"></v-img>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="12" sm="3" class="mt-n6 pr-0">
          <v-toolbar flat outlined>
            <v-toolbar-title>
              <strong>Filter</strong>
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <v-divider vertical></v-divider>
            <v-btn icon class="ml-1">
              <v-icon color="#3853D8">mdi-sync</v-icon>
            </v-btn>
          </v-toolbar>
        </v-col>
        <v-col cols="12" sm="3" class="mt-n6 px-0">
          <v-toolbar flat outlined>
            <v-toolbar-title>
              SORT BY: <span>Price $-$$</span>
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn icon class="mr-4">
              <v-icon color="black">mdi-menu-down</v-icon>
            </v-btn>
          </v-toolbar>
        </v-col>
        <v-col cols="12" sm="3" class="mt-n6 px-0">
          <v-toolbar flat outlined class="">
            <v-toolbar-title>SHOW: <span>12</span></v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn icon class="mr-4">
              <v-icon color="black">mdi-menu-down</v-icon>
            </v-btn>
          </v-toolbar>
        </v-col>
        <v-col cols="12" sm="3" class="mt-n6 pl-0">
          <v-toolbar flat outlined>
            <v-btn icon class="mr-1">
              <v-icon color="#3853D8">mdi-apps</v-icon>
            </v-btn>
            <v-divider vertical></v-divider>
            <v-btn icon class="mx-1">
              <v-icon color="grey">mdi-format-list-bulleted</v-icon>
            </v-btn>
            <v-divider vertical></v-divider>
            <v-toolbar-title class="ml-2">
              <strong>COMPARE: </strong>
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <v-badge color="#3853D8" content="3" class="mr-2"></v-badge>
          </v-toolbar>
        </v-col>
        <v-col cols="3" class="py-0 pr-0 mt-n3">
          <v-card flat outlined tile>
            <v-toolbar flat>
              <v-icon color="black" class="mr-2">mdi-chevron-down</v-icon>
              <strong>CATEGORIES</strong>
              <v-spacer></v-spacer>
              <v-icon color="grey" small>mdi-close</v-icon>
            </v-toolbar>
            <v-list dense class="mt-n5">
              <v-list-item v-for="style in styles" :key="style.title">
                <v-list-item-content>
                  <v-list-item-title v-text="style.title" class="ml-8"></v-list-item-title>
                </v-list-item-content>
                <v-list-item-action>
                  <v-list-item-subtitle v-text="style.count"></v-list-item-subtitle>
                </v-list-item-action>
              </v-list-item>
            </v-list>
          </v-card>
          <v-card flat outlined tile>
            <v-toolbar flat>
              <v-icon color="black" class="mr-2">mdi-chevron-down</v-icon>
              <strong>PRICE</strong>
              <v-spacer></v-spacer>
              <v-icon color="grey" small>mdi-close</v-icon>
            </v-toolbar>
            <v-toolbar flat>
              <v-text-field placeholder="$50" filled rounded dense class="mx-2"></v-text-field>
              <v-text-field placeholder="$1900" filled rounded dense class="mx-2"></v-text-field>
            </v-toolbar>
            <v-range-slider color="blue" max="40" min="-30"></v-range-slider>
          </v-card>
          <v-card falt outlined tile>
            <v-toolbar flat>
              <v-icon color="black" class="mr-2">mdi-chevron-down</v-icon>
              <strong>BRAND</strong>
              <v-spacer></v-spacer>
              <v-icon color="grey" small>mdi-close</v-icon>
            </v-toolbar>
            <v-list dense class="mt-n5">
              <v-list-item v-for="brand in brands" :key="brand.title">
                <v-list-item-content>
                  <v-list-item-title v-text="brand.title" class="ml-6"></v-list-item-title>
                </v-list-item-content>
                <v-list-item-action>
                  <v-checkbox color="primary" v-model="brand.state"></v-checkbox>
                </v-list-item-action>
              </v-list-item>
            </v-list>
          </v-card>
          <v-card flat outlined tile>
            <v-toolbar flat>
              <v-icon color="black" class="mr-2">mdi-chevron-down</v-icon>
              <strong>COLOR</strong>
              <v-spacer></v-spacer>
              <v-icon color="grey" small>mdi-close</v-icon>
            </v-toolbar>
            <v-chip-group column multiple>
              <v-chip filter outlined color="black" text-color="black" class="ml-2"></v-chip>
              <v-chip filter color="#E6E6E6" text-color="black"></v-chip>
              <v-chip filter color="#FFB500" text-color="white"></v-chip>
              <v-chip filter color="#F27229" text-color="white"></v-chip>
              <v-chip filter color="#EB3427" text-color="white"></v-chip>
              <v-chip filter color="#923FA3" text-color="white"></v-chip>
              <v-chip filter color="#3A51DF" text-color="white" class="ml-2"></v-chip>
              <v-chip filter color="#23A7F5" text-color="white"></v-chip>
              <v-chip filter color="#5EB524" text-color="white"></v-chip>
              <v-chip filter color="#7C5F4D" text-color="white"></v-chip>
              <v-chip filter color="black" text-color="white"></v-chip>
              <v-chip filter color="lime" text-color="white"></v-chip>
            </v-chip-group>
          </v-card>
          <v-card flat outlined>
            <v-toolbar flat>
              <v-icon color="black" class="mr-2">mdi-chevron-down</v-icon>
              <strong>SIZE</strong>
              <v-spacer></v-spacer>
              <v-icon color="grey" small>mdi-close</v-icon>
            </v-toolbar>
            <v-chip-group column multiple active-class="blue white--text" class="ml-2">
              <v-chip v-for="size in sizes" :key="size" :value="size" class="size">
                {{ size }}
              </v-chip>
            </v-chip-group>
          </v-card>
        </v-col>
        <v-col cols="9" class="mt-n3">
          <v-row>
            <v-col cols="12" sm="4" v-for="(cloth, i) in clothes" :key="i" :class="cloth.class">
              <v-hover v-slot:default="{hover}">
                <v-card height="300" align="center" flat outlined tile>
                  <v-card-actions>
                    <v-spacer></v-spacer>
                    <v-btn color="black" small dark>{{cloth.sold}}</v-btn>
                  </v-card-actions>
                  <v-img :src="cloth.image" width="200" height="200" contain></v-img>
                  <v-card-text class="mt-n4">
                    <strong :class="hover ? 'red--text' : 'black--text'">{{cloth.title}}</strong>
                  </v-card-text>
                  <v-expand-transition>
                    <div v-if="hover" class="d-flex transition-fast-in-fast-out blue v-card--reveal display-3 white--text" style="height: 100%;">
                      <v-btn rounded color="white">
                        <v-icon>mdi-cart-outlined</v-icon>
                        Buy 
                      </v-btn>
                      <v-btn fab small color="white" class="ml-2">
                        <v-icon color="black">mdi-content-copy</v-icon>
                      </v-btn>
                      <v-btn fab small color="white" class="ml-2">
                        <v-icon color="black">mdi-heart-outline</v-icon>
                      </v-btn>
                    </div>
                  </v-expand-transition>
                </v-card>
              </v-hover>
            </v-col>
          </v-row>
        </v-col>
        <v-col cols="12" sm="3" class="mt-n3 pr-0 pb-0">
          <v-toolbar flat outlined>

          </v-toolbar>
        </v-col>
        <v-col cols="12" sm="3" class="mt-n3 px-0 pb-0">
          <v-toolbar flat outlined>
            <v-btn icon class="mr-1">
              <v-icon color="grey">mdi-chevron-up</v-icon>
            </v-btn>
            <v-divider vertical></v-divider>
          </v-toolbar>
        </v-col>
        <v-col cols="12" sm="3" class="mt-n3 px-0 pb-0">
          <v-toolbar flat outlined class="text-center">
            <v-pagination v-model="page" :length="4">
            </v-pagination>
          </v-toolbar>
        </v-col>
        <v-col cols="12" sm="3" class="mt-n3 pl-0 pb-0">
          <v-toolbar flat outlined>
            <v-btn icon class="mr-1">
              <v-icon color="grey">mdi-chevron-down</v-icon>
            </v-btn>
            <v-divider vertical></v-divider>
          </v-toolbar>
        </v-col> 
      </v-row>
    </v-card>
    <v-card color="#EFF0F2" height="250px" tile flat dark class="d-flex align-center justify-center mt-n10 card2">
      <v-row>
        <v-col cols="12" sm="12">
          <h4 class="text-center black--text mt-10">SUBSCRIBE TO OUR NEWSLETTER</h4>
        </v-col>
        <v-col cols="12" sm="12">
          <h6 class="text-center grey--text">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Repudiandae nihil praesentium ipsam voluptatem officia eius? Nemo tenetur esse aspernatur repellat, beatae a accusamus magni alias voluptatum nostrum, odit quam numquam.
          </h6>
        </v-col>
        <v-col cols="12" sm="12">
          <v-card flat color="transparent" class="d-flex justify-center">
            <v-text-field placeholder="Enter Your Email" rounded class="shrink" background-color="grey" filled append-icon="mdi-email-outline" dense></v-text-field>
          </v-card>
        </v-col>
      </v-row>
    </v-card>
  </v-container>
</template>

<script>
export default {
  name: 'Dashboard-View',
  data: () => ({
    page: 1,
    items: [
      {
        text: "Home",
        disabled: false,
        href: "breadcrumbs_home"
      },
      {
        text: "Catalog",
        disabled: false,
        href: "breadcrumbs_catalog"
      },
      {
        text: "Men",
        disabled: false,
        href: "breadcrumbs_men"
      },
      {
        text: "Shoes",
        disabled: false,
        href: "breadcrumbs_shoes"
      }
    ],
    styles: [
      {
        title: "Lifestyle",
        count: '1'
      },
      {
        title: "Football",
        count: '15'
      },
      {
        title: "Basketball",
        count: '11'
      },
      {
        title: "Golf",
        count: '15'
      },
      {
        title: "Skateboarding",
        count: '22'
      },
      {
        title: "Soccer",
        count: '32'
      },
      {
        title: "Training & Gym",
        count: '45'
      },
      {
        title: "Running",
        count: '23'
      },
    ],
    brands: [
      {
        title: 'Lifestyle',
        state: true,
      },
      {
        title: 'Running',
        state: false,
      },
      {
        title: 'Training & Gym',
        state: true,
      },
      {
        title: 'Basketball',
        state: false,
      },
    ],
    sizes: [
      '35', '36', '37', '38', '39', '40', '41', '42', '43', '44', '45', '46'
    ],
    clothes: [
      {
        class: 'pa-0',
        sold: '-20%',
        image: '/assets/images/1.png',
        title: 'KD 8 EXT',
        price: '$ 145.00'
      },
      {
        class: 'pa-0',
        sold: '-30%',
        image: '/assets/images/2.png',
        title: 'Jordan Galaxy',
        price: '$ 599.00'
      },
      {
        class: 'py-0 pl-0',
        sold: '-14%',
        image: '/assets/images/3.png',
        title: 'Jordan Cosmos',
        price: '$ 140.00'
      },
      {
        class: 'pa-0',
        sold: '-18%',
        image: '/assets/images/4.png',
        title: 'KD 8 EXT Premium',
        price: '$ 180.00'
      },
      {
        class: 'pa-0',
        sold: '-20%',
        image: '/assets/images/5.png',
        title: 'KD 8 EXT',
        price: '$ 145.00'
      },
      {
        class: 'py-0 pl-0',
        sold: '-35%',
        image: '/assets/images/6.png',
        title: 'KD 8 EXT Pro',
        price: '$ 490.00'
      },
      {
        class: 'pa-0',
        sold: '-20%',
        image: '/assets/images/7.png',
        title: 'KD 8 EXT',
        price: '$ 145.00'
      },
      {
        class: 'pa-0',
        sold: '-17%',
        image: '/assets/images/8.png',
        title: 'Nike SB Trainerendor Leathe',
        price: '$ 145.00'
      },
      {
        class: 'py-0 pl-0',
        sold: '-22%',
        image: '/assets/images/9.png',
        title: 'Air Jordan Spike 40 iD',
        price: '$ 220.00'
      },
      {
        class: 'pa-0',
        sold: '-18%',
        image: '/assets/images/10.png',
        title: 'Nike Air Footscape Magista Flyknit',
        price: '$ 245.00'
      },
      {
        class: 'pa-0',
        sold: '-40%',
        image: '/assets/images/11.png',
        title: 'Nike Air Zoom Huarache 2k4',
        price: '$ 245.00'
      },
      {
        class: 'py-0 pl-0',
        sold: '-13%',
        image: '/assets/images/12.png',
        title: 'Jordan Horizon',
        price: '$ 230.00'
      },
      {
        class: 'pa-0',
        sold: '-15%',
        image: '/assets/images/13.png',
        title: 'Air Jordan xx9 Low',
        price: '$ 185.00'
      },
      {
        class: 'pa-0',
        sold: '-10%',
        image: '/assets/images/14.png',
        title: 'LeBron XIII Premium AS iD',
        price: '$ 265.00'
      },
      {
        class: 'py-0 pl-0',
        sold: '-19%',
        image: '/assets/images/15.png',
        title: 'Air Jordan 1 Retro High Nouveau',
        price: '$ 190.00'
      },
      {
        class: 'pa-0',
        sold: '-16%',
        image: '/assets/images/16.png',
        title: 'Nike Air Presto',
        price: '$ 175.00'
      },
      {
        class: 'pa-0',
        sold: '-10%',
        image: '/assets/images/17.png',
        title: 'KD 8 Premium AS iD',
        price: '$ 245.00'
      },

    ]
  })
}
</script>

<style>
.container {
  padding: 0px !important;
}

.v-btn.withoutupercase{
  text-decoration: none;
}

.v-chip.v-size--default {
  border-radius: 50px !important;
  font-size: 14px !important;
  height: 40px !important;
  width: 40px !important;
}
.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: .5;
  position: absolute;
  width: 100%;
}
.card1{
  z-index: 10;
}
.card2{
  z-index: 1;
}
</style>