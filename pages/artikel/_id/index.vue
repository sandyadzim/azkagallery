<template>
  <div class="cont-custom" style="margin-top: 86px">
    <div class="container-fluid bg-breadcrumb">
      <div class="container">
        <b-breadcrumb :items="bread" class="bg-breadcrumb"></b-breadcrumb>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailArtikel2',
  data: () => ({
    bread: [],
  }),
  mounted() {
    this._actionGetBread()
  },
  methods: {
    _actionGetBread() {
      this.bread = [
        {
          text: 'Home',
          href: '/',
        },
        {
          text: 'Artikel',
          href: '/artikel',
        },
        {
          text: this.$route.params.id,
          active: true,
        },
      ]
    },
  },
}
</script>
