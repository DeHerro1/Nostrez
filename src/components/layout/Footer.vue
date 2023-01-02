<template>
  <div class="footer_container">
    <div class="section footer py-5">
      <div class="col-lg-4 mt-4 px-3">
        <div>
          <img
            src="https://nostrez.com/public/uploads/all/A3XjD3FILjCB09EkjREJO0jcuYCJRNvb2kp5ouRZ.png"
            alt=""
            class="footer_logo"
          />
        </div>
        <p>
          <span
            >NoStrez.com is an E-Commerce Company providing Ghanaians with
            convenient virtual stores. We offer an easy-to-use online platform
            with many categories of services for shoppers and sellers to a
            unique variety of quality products.</span
          >
          <span>
            We are making a marketplace with a seamlessly "easy to order"
            process, making shopping stress-free, cost-effective, and an
            alternative to the traditional high street market.
          </span>
        </p>
        <p>
          <span>
            We offer Sellers a venue online which is easy to set up and will
            save overhead and fixed costs that have always been the foundation
            of traditional shops. Our NoStrez platform is built with one of the
            best digital and technology infrastructures providing shoppers and
            sellers with security and dependability.
          </span>
        </p>
        <div class="d-flex">
          <input
            type="email"
            class="form-control"
            id="exampleFormControlInput1"
            placeholder="Your Email Address"
          />
          <button class="btn btn-primary py-2 px-4">Subscribe</button>
        </div>
        <div class="d-flex justify-content-around pt-4">
          <img
            src="https://nostrez.com/public/assets/img/play.png"
            class="store"
            alt=""
          />
          <img
            src="https://nostrez.com/public/assets/img/app.png"
            class="store"
            alt=""
          />
        </div>
      </div>
      <div class="contact mt-4">
        <h4>CONTACT INFO</h4>
        <ul>
          <li class="d-flex flex-column">
            <span class="span1">Address:</span>
            <span class="span2">GK -0779-8001 NR BIS East Legon Hills</span>
          </li>
          <li class="d-flex flex-column">
            <span class="span1">Phone:</span>
            <span class="span2">024 232 5773</span>
          </li>
          <li class="d-flex flex-column">
            <span class="span1">Email:</span>
            <span class="span2">info@nostrez.com</span>
          </li>
        </ul>
      </div>
      <div class="mt-4 quick_links">
        <h4>QUICK LINKS</h4>
        <ul>
          <li><a href="#">Support Policy Page</a></li>
          <li><a href="#"> Return Policy Page</a></li>
          <li><a href="#"> About Us</a></li>
          <li><a href="#"> Privacy Policy Page</a></li>
          <li><a href="#"> Seller Policy</a></li>
          <li><a href="#"> Term Conditions Page</a></li>
          <li><a href="#"> Buyer Protection</a></li>
        </ul>
      </div>
      <div class="my_account mt-4">
        <h4>MY ACCOUNT</h4>
        <ul>
          <li><a href="#">Login</a></li>
          <li><a href="#">Order History</a></li>
          <li><a href="#">My Wishlist</a></li>
          <li><a href="#">Track Order</a></li>
        </ul>
        <h4 class="mt-5">BE A SELLER</h4>
        <button class="btn btn-primary py-2 px-4">Apply Now</button>
      </div>
    </div>
    <footer class="footer_bottom">
      <div class="section">
        <div class="d-flex justify-content-between">
          <p>© 2023 NoStrez.com. All rights reserved.</p>
          <ul class="d-flex">
            <li>
              <a href="#">
                <img
                  src="../../assets/img/facebook_Logo.png"
                  width="30px"
                  alt=""
                />
              </a>
            </li>
            <li>
              <a href="#" class="insta">
                <img
                  src="../../assets/img/instagram_logo.png"
                  width="30px"
                  alt=""
                />
              </a>
            </li>
            <li>
              <a href="#">
                <img
                  src="../../assets/img/youtube_logo.png"
                  width="56px"
                  height="30px"
                  alt=""
                />
              </a>
            </li>
            <li>
              <a href="#">
                <img
                  src="../../assets/img/linedin_logo.png"
                  width="30px"
                  alt=""
                />
              </a>
            </li>
          </ul>
          <ul>
            <li>
              <img
                src="https://nostrez.com/public/uploads/all/5bkNqAQne6miBuBynOdSwtxe5qlHWZNke5rIn4yt.png"
                alt=""
                width="200px"
              />
            </li>
          </ul>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  setup() {
    return {};
  },
};
</script>

<style scoped>
.footer_container {
  background-color: #111723;
  text-align: left;
}
p {
  font-size: 12px;
  color: #fff;
}
a,
a:hover {
  color: #fff;
  opacity: 0.5;
  text-decoration: none;
  cursor: pointer;
  transition: all 0.3s ease;
}
.span1 {
  opacity: 0.5;
}
.span2 {
  opacity: 0.7;
  color: #fff;
}
.footer {
  display: flex;
}
.footer_logo {
  height: 44px;
  margin-bottom: 20px;
}
.store {
  height: 40px;
  width: 120px;
}
h4 {
  font-size: 13px;
  margin-bottom: 24px;
  color: #fff;
}
ul {
  padding: 0;
}
li {
  list-style: none;
  padding-top: 10px;

  cursor: pointer;
  display: flex;
}
.contact {
  text-align: left;
  padding-right: 20px;
  margin-left: 90px;
}
.quick_links {
  padding-left: 20px;
  padding-right: 10px;
}
.my_account {
  padding-left: 40px;
}
.footer_bottom {
  padding: 10px 0;
  background-color: #0d111b !important;
}

.footer_bottom li {
  padding-right: 20px;
}

.footer_bottom p {
  margin-bottom: 20px;
}
.insta {
  background: #bd32a2;
  border-radius: 10px;
  padding: 2px;
}
</style>
