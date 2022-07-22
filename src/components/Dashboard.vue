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
              </v-col>
            </v-row>
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
  widows: 100%;
}
.card1{
  z-index: 10;
}
.card2{
  z-index: 1;
}
</style>