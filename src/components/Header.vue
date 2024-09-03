<template>
  <v-card color="basil">
    <v-card-title class="text-center justify-center py-6">
      <h1 class="font-weight-bold text-h2 text-basil">PDF 2 Go!</h1>
    </v-card-title>

    <v-tabs v-model="tab" bg-color="transparent" color="basil" grow>
      <v-tab
        v-for="item in items"
        :key="item"
        :text="item"
        :value="item"
      ></v-tab>
    </v-tabs>

    <v-tabs-window v-model="tab">
      <v-tabs-window-item v-for="item in items" :key="item" :value="item">
        <v-card color="basil" flat class="text-center justify-center">
          <v-card-text v-if="tab =='Live Editor'">
            {{descriptions.liveEditor}}
          </v-card-text>

          <v-card-text v-if="tab == 'Upload a Markdown Document'">{{descriptions.uploadMarkdown}}</v-card-text>
        </v-card>
      </v-tabs-window-item>
    </v-tabs-window>
  </v-card>
</template>

<script setup>
import { ref } from 'vue'

const tab = ref('Options')

const items = ['Live Editor', 'Upload a Markdown Document']
const descriptions = {
    liveEditor:'Write Markdown code in a live editor and instantly see how the resulting PDF will look in real-time.',
    uploadMarkdown:'Upload a Markdown document and preview the resulting PDF.'

}

</script>

<style scoped>
.bg-basil {
  background-color: #fffbe6 !important;
}
.text-basil {
  color: #356859 !important;
}
</style>
