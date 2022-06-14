<template>
  <!-- Footer -->
  <mdb-footer color="unique-color-dark" class="page-footer font-small pt-0">
    <div>&nbsp;</div>
    <mdb-container class="mt-5 mb-4 text-center text-md-left">
      <mdb-row class="mt-3">
        <mdb-col md="3" lg="3" xl="3" class="mb-4">
          <div
            class="text-uppercase font-weight-bold text-center"
            style="font-size: 16px"
          >
            <strong>Vale Side Limited</strong>
          </div>
          <div class="my-logo">
            <a href="/">
              <img src="@/assets/images/Vale Side Logo.svg" alt="logo" />
            </a>
          </div>
        </mdb-col>
        <mdb-col md="3" lg="3" xl="3" class="mb-4">
          <div class="text-uppercase font-weight-bold" style="font-size: 16px">
            <strong>Contact</strong>
          </div>
          <p>Vale Side Limited</p>
          <p><a href="#!">Tel:01274 442 184</a></p>
          <p><a href="#!"> info@vale-side.co.uk</a></p>
        </mdb-col>
        <mdb-col md="3" lg="3" xl="3" class="mb-4">
          <div class="text-uppercase font-weight-bold" style="font-size: 16px">
            <strong>Location</strong>
          </div>

          <p><a href="#!">Vale Side Limited</a></p>
          <p><a href="#!">4 Talbot Street</a></p>
          <p><a href="#!">Bradford</a></p>
          <p><a href="#!">BD7 1LB</a></p>
        </mdb-col>
        <mdb-col md="2" lg="2" xl="2" class="mb-4">
          <div class="text-uppercase font-weight-bold" style="font-size: 16px">
            <strong>Navigate</strong>
          </div>
          <p>
            <a href="/"><i class="fas fa-home mr-3"></i>Home</a>
          </p>
          <p>
            <a href="/AboutUs"><i class="fas fa-envelope mr-3"></i>About</a>
          </p>
          <p>
            <a href="/OurContact"><i class="fas fa-phone mr-3"></i>Contact</a>
          </p>
          <p>
            <a href="/OurServices"><i class="fas fa-print mr-3"></i>Services</a>
          </p>
        </mdb-col>
      </mdb-row>
    </mdb-container>
    <div class="footer-copyright text-center py-3">
      <mdb-container fluid>
        <!-- <a href="#">Copyright © Vale-Side-Limited 2021</a> -->
      </mdb-container>
    </div>
  </mdb-footer>
  <!-- Footer -->
</template>
<script>
import { mdbFooter, mdbContainer, mdbRow, mdbCol } from "mdbvue";
export default {
  name: "FooterPage",
  components: {
    mdbFooter,
    mdbContainer,
    mdbRow,
    mdbCol,
  },
};
</script>
<style>
.my-logo {
  margin: auto;
  padding-top: 10px;
}
@media screen and (max-width: 768px) {
  .my-logo {
    margin: auto;
  }
}
.headr {
  text-align: center;
}
a:link {
  text-decoration: none;
}
.my-logo{
  height: 50px;
  width: 200px;
}

@media screen and (min-width: 768px) and (max-width: 1024px){
  .my-logo{
    padding-right: 35px;
  }
}

</style>