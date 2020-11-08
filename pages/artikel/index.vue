<template>
  <div class="cont-custom" style="margin-top: 86px">
    <div class="container-fluid bg-breadcrumb">
      <div class="container">
        <b-breadcrumb :items="items" class="bg-breadcrumb"></b-breadcrumb>
      </div>
    </div>
    <div class="container">
      <div class="row">
        <div class="col-md-12 mb-3 text-center">
          <h3>Artikel Kami</h3>
          <div style="border-bottom: 3px solid #f14436"></div>
        </div>
        <div v-for="(i, index) in 5" :key="index" class="col-md-12">
          <div class="card card-artikel p-3">
            <h4>Lorem, ipsum dolor sit amet consectetur adipisicing elit.</h4>
            <p>
              <img
                alt=""
                src="https://i.pinimg.com/originals/0c/3b/3a/0c3b3adb1a7530892e55ef36d3be6cb8.png"
                height="35"
                width="35"
              /><span>
                <a href="#" rel="author" itemprop="url"
                  ><span itemprop="name">Admin</span></a
                ></span
              ><span> | </span><span>Posted on</span>
              <time
                datetime="2020-05-21T04:50:40+00:00"
                itemprop="datePublished"
                >May 21, 2020</time
              >
            </p>
            <div class="row">
              <div class="col-md-4 text-center">
                <img
                  src="https://via.placeholder.com/300"
                  alt=""
                  class="img-fluid"
                />
              </div>
              <div class="col-md-8">
                <div class="d-flex align-items-start flex-column">
                  <div class="mb-auto p-2">
                    <p>
                      Lorem ipsum dolor sit amet consectetur adipisicing elit.
                      Doloribus excepturi minima alias ullam beatae dolores ut
                      doloremque? Iste, velit quo, facere, pariatur incidunt
                      mollitia fuga provident odit voluptate debitis blanditiis?
                      Lorem ipsum.
                    </p>
                  </div>
                  <div class="p-2">
                    <nuxt-link
                      :to="'/artikel/details?title=' + index + 1"
                      class="btn btn-outline-secondary"
                    >
                      Baca Selengkapnya
                    </nuxt-link>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Artikel',
  data: () => ({
    items: [
      {
        text: 'Home',
        href: '/',
      },
      {
        text: 'Artikel',
        active: true,
      },
    ],
  }),
}
</script>

<style scoped>
.card-artikel {
  border-radius: 12px;
  box-shadow: 0px 4px 5px rgba(0, 0, 0, 0.4);
  margin-bottom: 5px;
  margin-top: 5px;
  background-color: #fff;
}
</style>
