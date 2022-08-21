<template>
  <div>

    <header class="p-4 bg-gray-600">
      <div class="flex justify-between">
        <h1 class="text-3xl">North Shore SDA Church</h1>
        <div class="flex self-center space-x-8">
          <nuxt-link to="#">Home</nuxt-link>
          <nuxt-link to="#">About</nuxt-link>
          <nuxt-link to="#">Events</nuxt-link>
          <nuxt-link to="#">Livestream</nuxt-link>
        </div>
      </div>
    </header>

    <h1>hi</h1>
    <Carousel :images="images" />

    <footer>
      
    </footer>

  </div>
</template>

<script>
export default {
  data() {
    return {
      images: [
        {
          src: "https://images.pexels.com/photos/45201/kitty-cat-kitten-pet-45201.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500",
          link: "#"
        },
        {
          src: "https://images.unsplash.com/photo-1615789591457-74a63395c990?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8YmVhdXRpZnVsJTIwY2F0fGVufDB8fDB8fA%3D%3D&w=1000&q=80",
          link: "#"
        },
        {
          src: "https://media.npr.org/assets/img/2021/08/11/gettyimages-1279899488_wide-f3860ceb0ef19643c335cb34df3fa1de166e2761-s1100-c50.jpg",
        }
      ]
    }
  }
}
</script>