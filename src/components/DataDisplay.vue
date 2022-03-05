<script setup>
import {
  BIconHeartFill,
  BIconHeartHalf,
  BIconCalendarDateFill,
} from "bootstrap-icons-vue";
</script>


<template>
  <div class="shadow p-pad p-mar w-full">
    <div class="font-bold text-slate-700 flex items-center gap-x-4">
      <span class=""> <BIconCalendarDateFill /> </span> : {{ cases?.date }}
    </div>
    <div class="text-red-400 flex items-center gap-x-4">
      <span class="text-slate-700"> <BIconHeartFill /> </span> : +
      {{ cases?.positive }}
    </div>
    <div class="text-green-400 flex items-center gap-x-4">
      <span class="text-slate-700"><BIconHeartHalf /></span> : -
      {{ cases?.negative }}
    </div>
    <div></div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cases: {},
      list: ["hi", "hello"],
    };
  },
  computed: {},
  created() {
    fetch("https://api.covidtracking.com/v1/us/current.json")
      .then((res) => res.json())
      .then((data) => (this.cases = data[0]));
  },
};
</script>

<style>
</style>