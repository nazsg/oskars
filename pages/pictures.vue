<template>
  <div class="pictures">
    <section>
      <h1>Photos</h1>
      <no-ssr>
        <LightGallery
          :images="images"
          :index="index"
          :disable-scroll="true"
          @close="index = null"
        />
      </no-ssr>

      <ul>
        <li>
          <a
            href="#"
            v-for="(thumb, thumbIndex) in images"
            :key="thumbIndex"
            @click="index = thumbIndex"
          >
            <img :src="'/gallery/pic' + thumb.id + '_sm.jpg'" :alt="thumb.title" />
          </a>
        </li>
      </ul>
    </section>
  </div>
</template>

<script>
export default {
  head: {
    title: 'Oskars Barbers, in Herne Bay Kent',
    meta: [
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      {
        hid: 'description',
        name: 'description',
        content: 'Barbers for men in the high street of Herne Bay in Kent.',
      },
    ],
  },
  data() {
    return {
      path: '/preview/oskars',
      images: [
        { id: 1, title: 'image 1', url: '/gallery/pic1.jpg' },
        { id: 2, title: 'image 2', url: '/gallery/pic2.jpg' },
        { id: 3, title: 'image 3', url: '/gallery/pic3.jpg' },
        { id: 4, title: 'image 4', url: '/gallery/pic4.jpg' },
        { id: 5, title: 'image 5', url: '/gallery/pic5.jpg' },
        { id: 6, title: 'image 6', url: '/gallery/pic6.jpg' },
        { id: 7, title: 'image 7', url: '/gallery/pic7.jpg' },
        { id: 8, title: 'image 8', url: '/gallery/pic8.jpg' },
        { id: 9, title: 'image 9', url: '/gallery/pic9.jpg' },
        { id: 10, title: 'image 10', url: 'gallery/pic10.jpg' },
        { id: 11, title: 'image 11', url: '/gallery/pic11.jpg' },
        { id: 12, title: 'image 12', url: '/gallery/pic12.jpg' },
        { id: 13, title: 'image 13', url: '/gallery/pic13.jpg' },
        { id: 14, title: 'image 14', url: '/gallery/pic14.jpg' },
        { id: 15, title: 'image 15', url: '/gallery/pic15.jpg' },
        { id: 16, title: 'image 16', url: '/gallery/pic16.jpg' },
        { id: 17, title: 'image 17', url: '/gallery/pic17.jpg' },
        { id: 18, title: 'image 18', url: '/gallery/pic18.jpg' },
      ],
      index: null,
      thumbs: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18],
    }
  },
}
</script>

<style lang="scss" scoped>
ul {
  list-style-type: none;
  li {
    text-align: center;
    a {
      padding: 5px;
      img {
        border-radius: 15px;
        border: 1px solid rgb(105, 103, 103);
      }
    }
  }
}
</style>
