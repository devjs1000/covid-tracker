<template>
  <div class="shadow p-pad ">
  <router-link to="/" class="link p-mar" >Home</router-link>
  <router-link to="/about" class="link p-mar">About</router-link>
  </div>
</template>

<script>
export default {

}
</script>

<style>
.p-pad{
    @apply px-4 py-2;
}

.p-mar{
    @apply mx-4 my-2;
}


.link{
    @apply text-teal-500;
}
</style>