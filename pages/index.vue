<template>
  <MainLayout page-title="Schedule Activity">
    <Card/>
    <Calender @click="showCal()"/>
    <!-- <Cardtimer/> -->
    <div v-if="state.showCalender">
      <Calendarcard/>
    </div>
    <Buttonbottom>
      <Button label="Go to Checkout" :is-disabled="true"/>
    </Buttonbottom>
  </MainLayout>
</template>

<script setup>
import MainLayout from '~/Layout/Mainlayout.vue';
import Cardtimer from '~/components/Cardtimer.vue';
import Calender from '~/components/sections/Calender.vue';
import { reactive } from 'vue';
import Buttonbottom from '~/components/Buttonbottom.vue';
import Button from '~/components/Button.vue'

let state = reactive({ showCalender: false, showTimeline: false})

function showCal() {
  state.showCalender = true;
}
</script>
