<template>
  <div>
    <div>
      <div>
        <div class="image-section rel mb-3">
          <div class="for-desk">
            <img
              src="~assets/images/ContactUs/Contact-us.jpg"
              alt=""
              class="img-fluid"
            />
            <div class="banner-text">
              CONTACT <span class="color-red">US</span>
            </div>
          </div>
          <div class="for-mob">
            <img
              src="~assets/images/ContactUs/Contact-us-mobile.jpg"
              alt=""
              class="img-fluid"
            />
            <div class="banner-text">
              CONTACT<span class="color-red">US</span>
            </div>
          </div>
        </div>
        <div class="address">
          <b-container>
            <b-row>
              <b-col lg="6" md="6" sm="12">
                <div class="cards text-align:right">
                  <h2 class="header-title">Contact</h2>

                  <p><span></span>Tel:01274 442 184</p>

                  <p>Email: info@vale-side.co.uk</p>
                </div>
              </b-col>
              <b-col lg="6" md="6" sm="12">
                <div class="cards">
                  <h5 class="header-title">Address</h5>

                  <p><span></span>Vale Side Limited</p>

                  <p><span></span>4 Talbot Street</p>

                  <p><span></span>Bradford</p>
                  <p>BD7 1LB</p>
                </div>
              </b-col>
            </b-row>
          </b-container>
        </div>
        <div>&nbsp;</div>

        <b-container>
          <b-row>
            <b-col>
              <div>
                <iframe
                  src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2356.6902870598547!2d-1.775455984621286!3d53.79499968007553!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x487be6b0b04b7437%3A0xf1f278f8e6ea4f42!2s4%20Talbot%20St%2C%20Fieldhead%20Business%20Centre%2C%20Bradford%20BD7%201LB%2C%20UK!5e0!3m2!1sen!2sin!4v1634398702314!5m2!1sen!2sin"
                  width="100%"
                  height="600"
                  style="border: 0"
                  allowfullscreen=""
                  loading="lazy"
                ></iframe>
              </div>
            </b-col>
          </b-row>
        </b-container>
      </div>
      <div>&nbsp;</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
};
</script>
<style lang="scss">
.for-desk {
  img {
    width: 100%;
    height: 450px;
    overflow: hidden;
  }
}

.service,
h6 {
  padding-left: 10%;
  color: #fff;
}
.cards {
  border: none;
  margin: auto;
  padding: 10px;
}
.address {
  padding-bottom: 20px;
  margin: 5px;
}
p {
  font-weight: 500;
}
.header-title {
  color: #000;
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