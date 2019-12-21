<template>
    <v-container :style="{'overflow-y':'scroll','height':'80vh'}">
        <v-timeline>
          <v-timeline-item>
              <v-lazy :options="{threshold: 0.5}" transition="fade-transition">
                  <v-card>
              <v-card-title>Kedarkantha</v-card-title>
              <v-card-text>
                <v-img src="https://picsum.photos/id/11/1920/1080">
                </v-img>
              </v-card-text>
            </v-card>
              </v-lazy>
          </v-timeline-item>

          <v-timeline-item>
              <v-lazy>
                  <v-card>
              <v-card-title>Kedarkantha</v-card-title>
              <v-card-text>
                <v-img src="https://picsum.photos/id/11/1920/1080">
                </v-img>
              </v-card-text>
            </v-card>
              </v-lazy>
          </v-timeline-item>

          <v-timeline-item>
              <v-lazy transition="fade-transition">
                  <v-card>
              <v-card-title>Kedarkantha</v-card-title>
              <v-card-text>
                <v-img src="https://picsum.photos/id/11/1920/1080">
                </v-img>
              </v-card-text>
            </v-card>
              </v-lazy>
          </v-timeline-item>
        </v-timeline>
    </v-container>
</template>
<style scoped>
    #timeline{
        overflow-y: scroll;
    }
</style>
