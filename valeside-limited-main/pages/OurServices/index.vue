<template>
  <div>
    <div class="service-section">
      <div class="image-section rel mb-5">
        <div class="for-desk">
          <img
            src="~assets/images/Services/service-img-banner.jpg"
            alt=""
            class="img-fluid"
          />
          <div class="banner-text">
            OUR <span class="color-red">SERVICES</span>
          </div>
        </div>
        <div class="for-mob">
          <img
            src="~assets/images/Services/service-mob-img.jpg"
            alt=""
            class="img-fluid"
          />
          <div class="banner-text">
            OUR <span class="color-red">SERVICES</span>
          </div>
        </div>
      </div>
      <div>
        <b-container>
          <b-row align-content="center">
            <b-col lg="2" md="2" sm="12"></b-col>
            <b-col lg="8" md="8" sm="12">
              <div class="py-4">
                <h1 class="heading font-weight-medium" align="center">
                  SERVICES AVAILABLE
                </h1>
                <p>
                  With pure dedication to the finest craftsmanship, clients can
                  consistently expect a solid commitment to quality, strong work
                  ethic, and punctuality. Our personalized options and wide
                  range of prices cater to every budget, so you’re sure to find
                  the solutions you need. Take a look below at all of the
                  services that we offer and get in touch today.
                </p>
                <h5>A Few Highlights</h5>
                <p>
                  As a dedicated team of contractors, it gives us great pride to
                  be able to call these projects our own. Whatever the size or
                  time commitment of each project, our flexibility and strong
                  work ethic allows us to carefully plan ahead in order to meet
                  deadlines while delivering high quality solutions that are
                  built to last. Take a look at some sample projects below.
                </p>
                <h5>BATHROOMS</h5>
                <p>Some of our Bathrooms we have completed over the years.</p>
                <h5>KITCHENS</h5>
                <p>Some of our Kitchens we have installed over the years.</p>
                <h5>GARDEN ROOMS</h5>
                <p>
                  This is a collection of the Bespoke Garden Rooms we have
                  specifically built around each customer’s needs.
                </p>
                <h5>RENOVATION</h5>
                <p>
                  This is a collection of the renovation projects we have been
                  involved in.
                </p>
              </div>
            </b-col>
            <b-col lg="2" md="2" sm="12"></b-col>
          </b-row>
        </b-container>
      </div>
      <div>&nbsp;</div>
    </div>
  </div>
</template>

<script >
export default {
  data() {
    return {};
  },
};
</script>

<style lang="scss">
@import "~assets/scss/_variable";
.service-section {
  .image-section {
    .banner-text {
      margin: 0;
      position: absolute;
      bottom: 10%;
      right: 0%;
      transform: translate(-50%, -50%);
      color: white;
      z-index: 1;
      font-size: 30px;
    }
  }
}
.for-desk {
  display: block;
  img {
    height: 450px;
    width: 100%;
    overflow: hidden;
  }
}
.for-mob {
  display: none;
}

.color-red {
  color: #ef4136;
}
.rel {
  position: relative;
}

// for mobile
@media only screen and (max-width: 767px) {
  .for-desk {
    display: none;
  }
  .for-mob {
    display: block;
  }
  img {
    height: 100%;
    width: 100%;
    overflow: hidden;
  }
  .service-section {
    .image-section {
      .banner-text {
        top: 50%;
        left: 50%;
      }
    }
  }
}

.service,
h6 {
  color: #000;
}
p {
  font-weight: 500;
  line-height: 1.8em;
}
</style>