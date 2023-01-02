<template>
  <div class="header_container">
    <div class="top_header_container">
      <div
        class="top_header section d-flex justify-content-between align-items-center"
      >
        <div class="d-flex">
          <select class="form-select" aria-label="Default select example">
            <option value="1" selected>
              <p>English</p>
            </option>
            <option value="2">Chinese</option>
            <option value="3">French</option>
          </select>
          <!-- 💶 -->
          <select
            class="form-select currency"
            aria-label="Default select example"
          >
            <option value="1">U.S.Dollar($)</option>
            <option value="2" selected>Ghana Cedi (GHS)</option>
          </select>
        </div>
        <div>
          <ul class="d-flex m-0">
            <li>
              <span class="material-icons pt-1 help call_icon"> call </span>
              <span class="help"> Help line</span>
              <span>024 232 5773</span>
            </li>
            <li class="mx-4 login_btn">Login</li>
            <li>Registration</li>
          </ul>
        </div>
      </div>
    </div>
    <div class="sticky-top main_header_container">
      <div class="d-flex main_header section align-items-center">
        <div class="pr-5">
          <img
            src="https://nostrez.com/public/uploads/all/hafj2fgnWjTUCKuOYkkJCiH3M684ZUJKpEV5W2P4.png"
            alt=""
            width="244px"
            height="40px"
          />
        </div>
        <div>
          <div class="input-group mt-2">
            <input
              type="text"
              class="form-control"
              placeholder="I am shopping for..."
              aria-label="Recipient's username"
              aria-describedby="basic-addon2"
            />
            <p class="search_cover">
              <span class="material-icons search_icon"> search </span>
            </p>
          </div>
        </div>
        <div class="main_header_options">
          <CompareSection />
        </div>
      </div>
    </div>
    <div class="section all_sections">
      <ul class="d-flex justify-content-evenly">
        <li>Home</li>
        <li>All categories</li>
        <li>Flash Sale</li>
        <li>Buyer Protection</li>
        <li>All Brands</li>
        <li>Coupons</li>
        <li>Blogs</li>
      </ul>
    </div>
  </div>
</template>

<script>
import CompareSection from './compareSection.vue';

export default {
  setup() {
    return {};
  },
  components: { CompareSection },
};
</script>

<style scoped>
.header_container {
  border-bottom: 1px solid #dee2e6;

  display: block;
  background: #fff;
  font-size: 13px;
  font-weight: 600;
}

.top_header_container {
  border-bottom: 1px solid #dee2e6;
}
.top_header {
  height: 45px;

  /* padding-top: 5px; */
}
li {
  list-style: none;
  padding-top: 10px;
  cursor: pointer;
  display: flex;
  height: 45px;
}
.form-select {
  border: none;
}
.call_icon {
  font-size: 16px;
}

.currency {
  width: 180px;
}

.help {
  margin-right: 5px;
}
.login_btn {
  border-left: 1px solid #dee2e6;
  border-right: 1px solid #dee2e6;
  padding: 10px 10px 0;
}
.search_cover {
  background: var(--primary);
  cursor: pointer;
  color: #fff;
  height: 42px;
  display: flex;
  align-items: center;
  padding: 10px 19px;
}

.search_cover:hover {
  background: var(--hov-primary);
}

.search_icon {
  font-size: 20px;
}

.main_header {
  height: 80px;
}
.main_header_container {
  border-bottom: 1px solid #dee2e6;
}
.main_header_options {
  padding-top: 20px;
  padding-left: 30px;
  display: flex;
}
.all_sections {
  width: 60%;
  position: sticky !important;
  position: -webkit-sticky !important;
  z-index: 100;
  top: 0;
}

.main_header_container,
.all_sections {
}

.all_sections li:hover {
  color: #000;
}
</style>
