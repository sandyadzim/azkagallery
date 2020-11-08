<template>
  <footer>
    <div
      class="container-fluid mt-5"
      style="background-color: #1b262c; color: #fff"
    >
      <div class="container">
        <div class="row">
          <div class="col-md-4 mt-5">
            <div class="">
              <!-- <img
                src="~/assets/img/logo tepian 1.png"
                alt="logo"
                height="70"
              /> -->
              <h2>AzkaGallery.id</h2>
            </div>
            <p class="mt-4" style="font-family: 'Poppins Italic">
              "Lorem ipsum dolor sit amet"
            </p>
            <div class="ml-md-5">
              <i class="p-1 fab fa-facebook" style="font-size: 40px"></i>
              <i class="p-1 fab fa-instagram" style="font-size: 40px"></i>
            </div>
          </div>
          <div class="col-md-4 mt-5">
            <p style="font-family: 'Poppins Bold">Menu</p>
            <ul class="nav flex-column" style="font-family: 'Poppins Regular">
              <li class="nav-item">
                <nuxt-link
                  class="text-white nav-link pl-0"
                  target="_blank"
                  to="/produk"
                  >Produk</nuxt-link
                >
              </li>
              <li class="nav-item">
                <nuxt-link
                  class="text-white nav-link pl-0"
                  target="_blank"
                  to="/artikel"
                  >Artikel</nuxt-link
                >
              </li>
              <li class="nav-item">
                <nuxt-link
                  class="text-white nav-link pl-0"
                  target="_blank"
                  to="/testimoni"
                  >Testimoni</nuxt-link
                >
              </li>
              <li class="nav-item">
                <nuxt-link class="text-white nav-link pl-0" to="/video"
                  >Video</nuxt-link
                >
              </li>
            </ul>
          </div>
          <div class="col-md-4 mt-5">
            <p style="font-family: 'Poppins Bold">Kontak Kami</p>
            <ul class="nav flex-column" style="font-family: 'Poppins Regular">
              <li class="nav-item">
                <p>
                  JL. Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                  Reprehenderit illum, unde distinctio recusandae quasi
                </p>
              </li>
              <li class="nav-item">
                <p>Email: lorem@gmail.com</p>
              </li>
              <li class="nav-item">
                <p>Telp/Hp: 0541 xxx / 0812 xxxx xxx</p>
              </li>
            </ul>
          </div>
        </div>
      </div>
      <div class="row mt-5 pb-3">
        <div
          class="col text-center text-white"
          style="font-family: 'Poppins Bold"
        >
          Copyright © {{ year }} • All rights reserved • AzkaGallery.id
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  data: () => ({
    year: '',
  }),
  mounted() {
    this._actionYear()
  },
  methods: {
    _actionYear() {
      return (this.year = new Date().getFullYear())
    },
  },
}
</script>
