<template>
  <footer>
    <div class="container">
      <div class="row">
        <div class="col-3 p-5">
          <img class="pb-3" src="../../public/images/white-logo-2.png" alt="">
          <p>When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper</p>
        </div>
        <div class="col-3 p-5">
          <ul>
            <h6 class="fw-bolder">Quick Links</h6>
            <li>
              <p><a href="#">Services</a></p>
            </li>
            <li>
              <p><a href="#">Contact</a></p>
            </li>
            <li>
              <p><a href="#">Blog</a></p>
            </li>
          </ul>
        </div>
        <div class="col-3 p-5">
          <ul>
            <h6 class="fw-bolder">Resoirces</h6>
            <li>
              <p><a href="#">Art Design</a></p>
            </li>
            <li>
              <p><a href="#">Computer</a></p>
            </li>
            <li>
              <p><a href="#">IT News</a></p>
            </li>
            <li>
              <p><a href="#">Networking</a></p>
            </li>
            <li>
              <p><a href="#">Web Security</a></p>
            </li>
          </ul>
        </div>
        <div class="col-3 p-5">
          <ul>
            <h6 class="fw-bolder">Contact US</h6>
            <li>
              <p><span class="fw-bolder text-white">Address: </span>Patricia C. Amedee 4401 Waldeck Street Grapevine
                Nashville, Tx 76051</p>
            </li>
            <li>
              <p><span class="fw-bolder text-white">Phone: </span>+99 (0) 101 0000 888</p>
            </li>
            <li>
              <p><span class="fw-bolder text-white">Email: </span>Info@yourdomain.com</p>
            </li>
          </ul>
        </div>
      </div>
    </div>
    <div class="bottomFooter">
      <div class="container d-flex">
        <div class="copyright pt-4">
          <p>2020 Phlox. All Rights Reserved.</p>
        </div>
        <div class="social">

        </div>
      </div>
    </div>
  </footer>
</template>
  
<script>

export default {
  name: 'FooterApp',

}

</script>
  
<style lang="scss" scoped>
footer {
  width: 100%;

  background-image: linear-gradient(180deg, #08123d, #020332);
  color: white;
  ;
}

p {
  font-size: 0.8rem;
  color: grey;
  line-height: 0.9rem;
}

h6 {
  padding-bottom: 10px;

}

a {
  color: grey;
}

.bottomFooter {
  border-top: 1px solid rgb(85, 83, 83);
  height: 80px;
}
</style>