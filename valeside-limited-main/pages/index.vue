<template>
  <div>
    <Slider />
    <div>&nbsp;</div>
    <div class="main-content mt-0">
      <div class="our-container">
        <b-container class="fluid py-4">
          <b-row>
            <b-col lg="2" md="2" sm="12"> </b-col>
            <b-col lg="6" md="6" sm="12">
              <div class="py-4">
                <div>&nbsp;</div>
                <h5>Everything You Need</h5>
                <div>&nbsp;</div>
                <p>
                  <strong> Vale Side Limited</strong> has always operated under
                  strong values aimed at exceeding client needs. Our
                  communication channels are always open-our relationship with
                  our clients begins on the first day of contact.
                </p>
              </div>
            </b-col>
            <b-col lg="4" md="4" sm="12"> </b-col>
          </b-row>
        </b-container>
      </div>
      <div class="service-content">
        <b-container class="fluid py-4">
          <b-row>
            <b-col>
              <h1 class="text-center heading font-weight-medium">
                Services Available
              </h1>
              <p>
                With pure dedication to the finest craftsmanship, clients can
                consistently expect a solid commitment to quality, strong work
                ethic, and punctuality. Our personalized options and wide range
                of prices cater to every budget, so you’re sure to find the
                solutions you need. Take a look below at all of the services
                that we offer and get in touch today.
              </p>
            </b-col>
          </b-row>
          <div>
            <div class="projectimgs">
              <b-row>
                <b-col lg="6" md="6" sm="8" xs="12">
                  <div class="card">
                    <img src="~/assets/images/services4.jpg" alt="Image 3" />
                  </div>
                </b-col>

                <b-col lg="6" md="6" sm="8" xs="12">
                  <div class="card">
                    <img src="~/assets/images/services5.jpg" alt="Image 3" />
                  </div>
                </b-col>
              </b-row>
            </div>
          </div>
        </b-container>
      </div>
      <div>
        <div>
          <div class="address">
            <b-container>
              <h1 class="text-center heading font-weight-medium">
                Our Contact
              </h1>
              <h5 class="text-center">
                Should you wish to contact us and discuss an upcoming project
                then we would be delighted to hear from you.
              </h5>
              <b-row>
                <b-col lg="4" md="4" sm="4"></b-col>
                <b-col lg="4" md="4" sm="12">
                  <div class="cards text-center">
                    <h2 class="header-title">Contact</h2>

                    <p><span></span>Tel:01274 442 184</p>

                    <p>Email: info@vale-side.co.uk</p>
                  </div>
                </b-col>
                <b-col lg="4" md="4" sm="4"></b-col>
              </b-row>
              <b-row>
                <b-col lg="4" md="4" sm="4"></b-col>
                <b-col lg="4" md="4" sm="12">
                  <div class="cards text-center">
                    <h5 class="header-title">Address</h5>

                    <p><span></span>Vale Side Limited</p>

                    <p><span></span>4 Talbot Street</p>

                    <p><span></span>Bradford</p>
                    <p>BD7 1LB</p>
                  </div>
                </b-col>
                <b-col lg="4" md="4" sm="4"></b-col>
              </b-row>
            </b-container>
          </div>
          <div>&nbsp;</div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  return() {},
};
</script>
<style >
.heading {
  color: #000;
  font-weight: 300;
}
p {
  line-height: 1.8em;
}
.our-container {
  background-image: url("~/assets/images/about-bg.jpeg");
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
img {
  width: 100%;
  height: 100%;
  overflow: hidden;
}

@media only screen and (min-width: 575px) and (max-width: 767px){
  img {
    height: 100%;
    width: 150%;
    overflow: hidden;
  }
}
</style>