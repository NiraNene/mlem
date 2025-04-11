<script setup>
const showOverlay = ref(false)

const playFartAndShowCat = () => {
  const audio = new Audio('/farto.mp3')
  audio.play()
  showOverlay.value = true

  setTimeout(() => {
    showOverlay.value = false
  }, 1000)
}
</script>

<template>
  <div class="container mx-auto max-w-2xl mt-24 mb-24 px-4">
    <h1 class="text-4xl font-bold text-center mb-8">MLEM MLEM 😺✨</h1>
    <p class="text-center text-gray-300 mb-8">made by Nira with Cursor AI and Nuxt UI</p>


    <div>
      Pipik pipik
      <UButton size="xl" class="mb-8 text-xl font-bold" @click="playFartAndShowCat">
        CLICK ME IF YOU NOT GEJ
      </UButton>
    </div>

    <div class="space-y-6">
      <p class="text-lg">
        Kitties awe such pwecious wittle fwiends! 🐱 When dey do their gwaceful *mlem mlem* with their smol tongues,
        it's just too kawaii~ These fuffy companions bwing so much happiness to our homes with their silly zoomies and
        sweet purrrrrs! 🌟
      </p>
      <p class="text-lg">
        OwO! Whether they're chasing the mysterious red dot 🔴, snuggling in their favowite sunbeam ☀️, or making the
        cutest wittle faces when they want tweats, our kitty fwiends are both majestic and adowabwe at the same time!
        *nuzzles* 💕
      </p>
      <p class="text-lg">
        <strong>Evewy</strong> kitty has their own <strong>speshul pawsonality</strong>~ 🐾 From the
        <strong>smol</strong> beans doing their <strong>cwazy</strong> zoomies around the house
        to the wise elder <strong>floofs</strong> who are <strong>pwofessional</strong> nap-time experts! Their
        *<strong>mlem mlem</strong>* moments make our <strong>kokoros</strong> go
        <strong>doki doki</strong> with joy! 🥺💖
      </p>

      <div class="grid grid-cols-2 md:grid-cols-3 gap-4">
        <img src="https://i.kym-cdn.com/photos/images/newsfeed/001/878/329/dfa.jpg" alt="Surprised cat meme"
          class="w-full h-48 object-cover rounded-lg">
        <img src="https://i.kym-cdn.com/entries/icons/original/000/046/895/huh_cat.jpg" alt="Huh cat meme"
          class="w-full h-48 object-cover rounded-lg">
        <img src="https://i.kym-cdn.com/photos/images/newsfeed/002/652/460/d70.jpg" alt="Pop cat meme"
          class="w-full h-48 object-cover rounded-lg">
        <img src="https://i.kym-cdn.com/entries/icons/original/000/043/403/cover3.jpg" alt="Crying cat meme"
          class="w-full h-48 object-cover rounded-lg">
        <img src="https://i.kym-cdn.com/photos/images/newsfeed/002/247/947/e02.jpg" alt="Smiling cat meme"
          class="w-full h-48 object-cover rounded-lg">
        <img
          src="https://preview.redd.it/share-your-favourite-car-images-v0-ri5vim4xirfd1.jpeg?auto=webp&s=38b926a6d7099bb8bf348952536eaf1478c5b13c"
          alt="Cat with tongue out meme" class="w-full h-48 object-cover rounded-lg">
      </div>
    </div>
  </div>

  <Transition name="fade">
    <div v-if="showOverlay" class="fixed inset-0 bg-black z-50">
      <img
        src="https://preview.redd.it/share-your-favourite-car-images-v0-ri5vim4xirfd1.jpeg?auto=webp&s=38b926a6d7099bb8bf348952536eaf1478c5b13c"
        alt="Cat with tongue out meme" class="w-full h-full object-cover">
    </div>
  </Transition>
</template>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>