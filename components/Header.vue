<template>
  <div>
    <div class="row">
      <div class="col">
        <nav
          class="navbar navbar-expand-sm navbar-light bg-nav is-desktop fixed-top"
        >
          <div class="container">
            <nuxt-link to="/" class="navbar-brand text-white">
              Azka Gallery
            </nuxt-link>
            <!-- Desktop Menu -->
            <div class="d-none d-md-block d-lg-blocks">
              <ul class="navbar-nav text-white ml-auto">
                <li class="nav-item">
                  <a class="nav-link a-custom" href="#">Home</a>
                </li>
                <li class="nav-item">
                  <a class="nav-link a-custom" href="#">Produk</a>
                </li>
                <!-- <li class="nav-item">
                  <a class="nav-link a-custom" href="#">Video</a>
                </li> -->
                <li class="nav-item">
                  <a class="nav-link a-custom" href="#">Kontak Kami</a>
                </li>
                <li class="nav-item" :class="{ 'd-none': isShowBtn }">
                  <a
                    class="nav-link"
                    href="javascript:void(0)"
                    @click="btnSearch"
                  >
                    <i class="fas fa-search"></i>
                  </a>
                </li>
                <li
                  class="nav-item align-self-center"
                  :class="{ 'd-none': isShow }"
                >
                  <form>
                    <input
                      v-model="search"
                      type="text"
                      class="form-control"
                      placeholder="Pencarian"
                    />
                  </form>
                </li>
                <li
                  class="nav-item align-self-center"
                  :class="{ 'd-none': isShow }"
                >
                  <i
                    class="ml-2 far fa-times-circle"
                    style="cursor: pointer"
                    @click="disBtnSearch"
                  ></i>
                </li>
              </ul>
            </div>
            <!-- End Desktop Menu -->
            <!-- Mobile Menu -->
            <div
              v-b-toggle.sidebar-backdrop
              class="d-block d-md-none d-lg-none"
              style="background-color: #f14436; border-radius: 5px"
            >
              <i class="fas fa-bars text-white p-2" style="font-size: 21px"></i>
            </div>
            <b-sidebar
              id="sidebar-backdrop"
              :backdrop-variant="variant"
              bg-variant="dark"
              backdrop
              shadow
            >
              <div class="px-3 py-2">
                <form class="inline-form" @submit.prevent="_actionSearch">
                  <div class="input-group">
                    <input
                      v-model="search"
                      type="text"
                      class="form-control input-custom"
                      placeholder="Pencarian"
                    />
                    <div class="input-group-append">
                      <button class="btn" type="submit">
                        <i class="fa fa-search text-white"></i>
                      </button>
                    </div>
                  </div>
                </form>
                <div class="mt-4 mb-4">
                  <div>
                    <h5 class="text-white">Menu</h5>
                    <div
                      style="border-bottom: 1px solid #fff; width: 30%"
                    ></div>
                    <div v-for="(i, index) in menu" :key="index" class="m-2">
                      <a href="" class="row margin-row a-mobile">
                        <div class="mr-auto p-2 text-white">
                          <!-- <i class=""></i> -->
                          {{ i.title }}
                        </div>
                      </a>
                    </div>
                  </div>
                </div>
              </div>
            </b-sidebar>
            <!-- End Mobile Menu -->
          </div>
        </nav>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
  data: () => ({
    isShow: true,
    isShowBtn: false,
    search: '',
    variant: 'dark',
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
  methods: {
    btnSearch() {
      this.isShow = false
      this.isShowBtn = true
    },
    disBtnSearch() {
      this.isShow = true
      this.isShowBtn = false
    },
    _actionSearch() {
      // eslint-disable-next-line no-console
      console.log(this.search)
      this.search = ''
    },
  },
}
</script>

<style scoped>
.bg-nav {
  background-color: #1b262c;
  height: 86px;
}
.nav-link {
  color: #fff !important;
}
.input-custom {
  background-color: transparent;
  border: 0;
  border-bottom: 1px solid #fff;
  color: #fff;
}
.margin-row {
  margin-left: 0px !important;
  margin-right: 0px !important;
}
</style>
