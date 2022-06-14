<template>
  <div>
    <div>
      <div class="image-section rel mb-3">
        <div class="for-desk">
          <img
            src="~assets/images/AboutUs/About-us.jpg"
            alt=""
            class="img-fluid"
          />
          <div class="banner-text">ABOUT <span class="color-red">US</span></div>
        </div>
        <div class="for-mob">
          <img
            src="~assets/images/AboutUs/About-us-mobile.jpg"
            alt=""
            class="img-fluid"
          />
          <div class="banner-text">ABOUT <span class="color-red">US</span></div>
        </div>
      </div>
      <div class="main-content">
        <b-container class="fluid py-4 our-container">
          <b-row>
            <b-col lg="2" md="2" sm="12"> </b-col>
            <b-col lg="6" md="6" sm="12">
              <div class="py-4">
                <h1 class="heading font-weight-medium">
                  LEARN ABOUT OUR <br />
                  BUSINESS
                </h1>
                <div>&nbsp;</div>
                <h5>Everything You Need</h5>
                <div>&nbsp;</div>
                <p>
                  <strong>Vale Side Limited</strong> has always operated under
                  strong values aimed at exceeding client needs. Our
                  communication channels are always open—our relationship with
                  our clients begins on the first day of contact, and only ends
                  once they’re fully satisfied with our work.
                </p>
                <p>
                  When you hire our services, you can count on us for the
                  results you want and need. Get in touch today, and discover
                  the advantage of working with <br />
                  <strong>Vale Side Limited.</strong>
                </p>
              </div>
            </b-col>
            <b-col lg="4" md="4" sm="12"> </b-col>
          </b-row>
        </b-container>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  return() {},
};
</script>
<style lang="scss">
.heading {
  color: #000;
  font-weight: 300;
}
p {
  line-height: 1.8em;
}
.main-content {
  background-image: url("~/assets/images/about-bg.jpeg");
}
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

.for-desk {
  display: block;
  img {
    width: 100%;
    height: 450px;
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

  .image-section {
    .banner-text {
      top: 50%;
      left: 50%;
    }
  }
}
</style>