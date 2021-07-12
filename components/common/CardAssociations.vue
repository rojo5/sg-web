<template>
  <div class="p-4 max-w-lg">
   <div class="h-full  rounded-lg overflow-hidden">
     <!-- <img class="lg:h-48 md:h-36 w-full object-cover object-center" src="https://dummy}image.com/720x400" alt="Logo"> -->
      <!-- <img :src="`./carousel/${i}.jpg`" /> -->
      <img :src="require(`~/assets/images/associations/${association.logo}`)">
     <div class="p-6 bg-white">
      <h1 class="tracking-widest text-lg font-extrabold text-gray-900 mb-3">{{ association.title }}</h1>
      <p class="leading-relaxed mb-5"> {{ association.description }}</p>

      <a :href="association.link" target="_blank"><button class="inline-flex text-white bg-red-600 border-0 py-2 px-6 focus:outline-none hover:bg-red-800 rounded">Saber más</button></a>
     </div>
   </div>
  </div>
</template>

<script>
export default {
    name:'CardAssociatons',
    props: {
      association: {
        type: Object,
        required: true
      }
    }

}
</script>

<style>

</style>