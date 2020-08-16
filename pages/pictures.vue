<template>
  <div class="pictures">
    <section>
      <h1>Photos</h1>
      <client-only>
        <LightGallery :images="images" :index="index" :disable-scroll="true" @close="index = null" />
      </client-only>

      <ul>
        <li>
          <a
            href="#"
            v-for="(thumb, thumbIndex) in thumbs"
            :key="thumbIndex"
            @click="index = thumbIndex"
          >
            <img :src=" '/gallery/pic' + thumb + '_sm.jpg'" />
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
      { charset: 'utf-8' },
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      { hid: 'description', name: 'description', content: 'Barbers for men in the high street of Herne Bay in Kent.' }
    ]
  },   
  data() {
    return {
      path: '/preview/oskars',
      images: [
        { title: "img 1", url: "/gallery/pic1.jpg" },
        { title: "img 2", url: "/gallery/pic2.jpg" },
        { title: "img 3", url: "/gallery/pic3.jpg" },
        { title: "img 4", url: "/gallery/pic4.jpg" },
        { title: "img 5", url: "/gallery/pic5.jpg" },
        { title: "img 6", url: "/gallery/pic6.jpg" },
        { title: "img 7", url: "/gallery/pic7.jpg" },
        { title: "img 8", url: "/gallery/pic8.jpg" },
        { title: "img 9", url: "/gallery/pic9.jpg" },
        { title: "img 10", url: "gallery/pic10.jpg" },
        { title: "img 11", url: "/gallery/pic11.jpg" },
        { title: "img 12", url: "/gallery/pic12.jpg" },
        { title: "img 13", url: "/gallery/pic13.jpg" },
        { title: "img 14", url: "/gallery/pic14.jpg" },
        { title: "img 15", url: "/gallery/pic15.jpg" },
        { title: "img 16", url: "/gallery/pic16.jpg" },
        { title: "img 17", url: "/gallery/pic17.jpg" },
        { title: "img 18", url: "/gallery/pic18.jpg" },
      ],
      index: null,
      thumbs: [ 1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18]
    };
  }
};
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