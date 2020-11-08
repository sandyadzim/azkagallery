<template>
  <div class="cont-custom" style="margin-top: 100px">
    <div class="container-fluid">
      <no-ssr>
        <div v-swiper:mySwiper="swiperOption">
          <div class="swiper-wrapper">
            <div class="swiper-slide">
              <img
                src="@/assets/img/banner-1.jpg"
                alt=""
                class="img-fluid"
                style="border-radius: 10px"
              />
            </div>
            <div class="swiper-slide">
              <img
                src="@/assets/img/banner-2.jpg"
                alt=""
                class="img-fluid"
                style="border-radius: 10px"
              />
            </div>
          </div>
          <div slot="pagination" class="swiper-pagination"></div>
        </div>
      </no-ssr>
    </div>
    <div class="container">
      <hr />
      <div class="row">
        <div class="col-md-12 text-center">
          <h3>Menu</h3>
        </div>
        <div class="d-none d-md-block d-lg-block col-md-12">
          <div class="row text-center justify-content-center">
            <div
              v-for="(i, index) in menu"
              :key="index"
              class="mx-3 min-width-menu"
            >
              <nuxt-link to="/produk?page=1" class="a-custom-black">
                <div class="mb-3 mt-3">
                  <div>
                    <img
                      src="https://tepianteknologi.com/_nuxt/img/ALL.f7f6c9e.png"
                      alt=""
                      class="img-cat"
                    />
                  </div>
                  <span>{{ i.title }}</span>
                </div>
              </nuxt-link>
            </div>
          </div>
        </div>
        <div class="d-block d-md-none d-lg-none col-md-12">
          <div class="list">
            <div
              v-for="(j, index) in menu"
              :key="index"
              class="item mr-4 text-center"
            >
              <nuxt-link to="/produk?page=1" style="color: #000">
                <div class="mb-3 mt-3">
                  <div>
                    <img
                      src="https://tepianteknologi.com/_nuxt/img/ALL.f7f6c9e.png"
                      alt=""
                      class="img-cat"
                    />
                  </div>
                  <span>{{ j.title }}</span>
                </div>
              </nuxt-link>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="container">
      <hr />
      <div class="col-md-12 text-center">
        <h3>Lorem Ipsum</h3>
      </div>
      <no-ssr>
        <div v-swiper:mySwiper2="swiperOption2">
          <div class="swiper-wrapper">
            <div
              v-for="(item, index) in 10"
              :key="index"
              class="swiper-slide col-6 col-lg-2 col-md-3 m-3 card card-produk"
              style="place-content: center"
            >
              <div>
                <a style="text-decoration: none">
                  <div class="card-body pt-2" style="text-align-last: center">
                    <img
                      src="https://admin.tepianteknologi.com/images/produk/no-image.jpg"
                      alt="default-image"
                      class="img-fluid"
                    />
                  </div>
                  <div class="mt-1 p-2 text-center">
                    <p class="mb-1 txt-title">test</p>
                    <p class="badge badge-info text-white">test</p>
                    <p class="txt-price text-center">Rp 10.000</p>
                  </div>
                </a>
              </div>
            </div>
          </div>
          <div slot="pagination" class="swiper-pagination"></div>
        </div>
      </no-ssr>
    </div>
    <div class="container">
      <hr />
      <div class="col-md-12 text-center">
        <h3>Artikel</h3>
      </div>
      <div class="row">
        <div v-for="k in 4" :key="k" class="col-md-6 mb-2">
          <div class="card">
            <div class="card-body">
              <h5>
                <b>
                  Lorem ipsum dolor sit amet consectetur adipisicing elit.
                </b>
              </h5>
              <p>
                Lorem ipsum dolor sit amet, consectetur adipisicing elit. Velit
                quaerat corporis eum magni assumenda repellendus rerum
                voluptatum sit aspernatur, accusantium officia ullam vero
                laborum atque excepturi quo deleniti sint facere!...
              </p>
            </div>
          </div>
        </div>
        <div class="col-md-12 text-right">
          <nuxt-link to="/artikel" class="txt-see-more"
            >Lihat semua >></nuxt-link
          >
        </div>
      </div>
    </div>
    <div class="container-fluid cont-testimoni">
      <hr />
      <div class="col-md-12 text-center">
        <h3 class="text-white">Testimoni</h3>
      </div>
      <div class="container">
        <div class="row">
          <div v-for="l in 3" :key="l" class="col-md-4 mb-3">
            <div class="card align-items-center">
              <img
                src="https://i.pinimg.com/originals/0c/3b/3a/0c3b3adb1a7530892e55ef36d3be6cb8.png"
                alt=""
                class="img-fluid"
                style="width: 150px; height: auto"
              />
              <div class="col-md-12 text-center">
                <p><b>Sandy Rahmansyah</b></p>
                <p>
                  Lorem ipsum dolor sit amet consectetur adipisicing elit. Nulla
                  earum magnam ad molestias iure iste. Dolore veritatis sunt
                </p>
                <p style="font-family: Poppins Italic">Front End Developer</p>
              </div>
            </div>
          </div>
        </div>
        <div class="text-right pb-3">
          <nuxt-link to="/testimoni" class="txt-see-more-2"
            >Lihat semua >></nuxt-link
          >
        </div>
      </div>
    </div>
    <div class="container">
      <div class="col-md-12 text-center mt-4 mb-3">
        <h3>Video</h3>
      </div>
      <div style="border-top: 5px solid #f14436"></div>
      <iframe
        src="https://www.facebook.com/plugins/video.php?href=https%3A%2F%2Fwww.facebook.com%2FAzkagalleryIDBalikpapan%2Fvideos%2F699847884216105%2F&show_text=0&width=560"
        width="100%"
        height="500"
        style="border: none; overflow: hidden"
        scrolling="no"
        frameborder="0"
        allowTransparency="true"
        allowFullScreen="true"
      ></iframe>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data: () => ({
    swiperOption: {
      spaceBetween: 30,
      centeredSlides: true,
      autoplay: {
        delay: 3000,
        disableOnInteraction: false,
      },
      pagination: {
        el: '.swiper-pagination',
        clickable: true,
      },
      navigation: {
        nextEl: '.swiper-button-next',
        prevEl: '.swiper-button-prev',
      },
    },
    swiperOption2: {
      slidesPerView: 5.1,
      pagination: {
        el: '.swiper-pagination',
        clickable: true,
      },
      navigation: {
        nextEl: '.swiper-button-next',
        prevEl: '.swiper-button-prev',
      },
      breakpoints: {
        1024: {
          slidesPerView: 5.1,
        },
        768: {
          slidesPerView: 3.4,
        },
        640: {
          slidesPerView: 1.7,
        },
        320: {
          slidesPerView: 1.6,
        },
      },
    },
    menu: [
      {
        title: 'All',
      },
      {
        title: 'Artikel',
      },
      {
        title: 'Kerajinan Tanah Liat',
      },
      {
        title: 'Kerajinan Kayu  Jati',
      },
      {
        title: 'Video',
      },
      {
        title: 'Testimoni pelanggan',
      },
    ],
  }),
}
</script>

<style>
.img-cat {
  width: auto;
  height: 50px;
}
.min-width-menu {
  width: 8%;
}
.card-produk {
  border-radius: 12px;
  box-shadow: 0px 4px 5px rgba(0, 0, 0, 0.4);
  margin-bottom: 5px;
  margin-top: 5px;
  background-color: #fff;
  min-height: 310px;
}
.cont-testimoni {
  background-color: #f14436;
}
</style>
