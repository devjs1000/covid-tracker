<script setup>
import DataDisplay from "../components/DataDisplay.vue";
</script>

<template>
<div class="uni-center">
    <dataDisplay />

</div>
</template>

<script>
export default {
  components: { DataDisplay },
};
</script>

<style>
.uni-center {
  @apply grid place-items-center;
}
.p-text {
  @apply text-teal-500;
}
.p-bg {
  @apply bg-teal-500;
}
</style>