<template>
  <div class="cont-custom" style="margin-top: 86px">
    <div class="container-fluid bg-breadcrumb">
      <div class="container">
        <b-breadcrumb :items="bread" class="bg-breadcrumb"></b-breadcrumb>
      </div>
    </div>
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <div>
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
            <div>
              <div class="text-center mb-3">
                <img
                  src="https://via.placeholder.com/300"
                  alt=""
                  class="img-fluid"
                />
              </div>
              <p class="text-justify">
                Lorem ipsum dolor, sit amet consectetur adipisicing elit. Iste,
                nihil sunt consequuntur quam excepturi perspiciatis quisquam
                quis quia tenetur nostrum aliquid non a deserunt quas ad
                inventore recusandae consectetur vitae? Lorem ipsum dolor sit
                amet consectetur adipisicing elit. Impedit praesentium quas
                corrupti excepturi optio, magni ipsa suscipit! Ipsum nobis
                blanditiis necessitatibus provident aspernatur vitae inventore,
                quas quo, dolore quos natus! Lorem ipsum dolor, sit amet
                consectetur adipisicing elit. Impedit omnis earum nemo minima
                rerum non qui explicabo quis veritatis beatae id placeat porro
                nobis neque sunt, adipisci nihil, illum delectus. Lorem ipsum,
                dolor sit amet consectetur adipisicing elit. Atque qui quidem,
                quod architecto perspiciatis molestias exercitationem facilis
                vero nulla nostrum est accusamus voluptates fugit error illo
                consequuntur earum unde laudantium?
                <br />
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailArtikel',
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
          text: this.$route.query.title,
          active: true,
        },
      ]
    },
  },
}
</script>
