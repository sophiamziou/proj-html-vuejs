<script>
import AppNavbar from "./AppNavbar.vue";
import AppSearch from "./AppSearch.vue";
export default {
  components: {
    AppNavbar,
    AppSearch,
  },
  data() {
    return {
      togglesearch: false,
      menuItems: [
        {
          label: "HOMES",
          url: "#",
          active: true,
          sublabel: [
            "Main home",
            "Business coaching",
            "Blog divided",
            "Grid home",
            "Coaching events",
            "Wellness coaching",
            "Landing",
          ],
        },
        {
          label: "PAGES",
          url: "#",
          active: false,
          sublabel: [
            "About Us",
            "About me",
            "Become a coach",
            "Pricing plans",
            "Contact us",
            "Portfolio lists",
            "Portfolio layouts",
            "Portfolio singles",
          ],
        },
        {
          label: "BLOG",
          url: "#",
          active: false,
          sublabel: ["Standard lists", "Masonry", "Post types"],
        },
        {
          label: "SHOP",
          url: "#",
          active: false,
          sublabel: [
            "Product list",
            "Product single",
            "Shop layouts",
            "Shop pages",
          ],
        },
        {
          label: "EVENTS",
          url: "#",
          active: false,
          sublabel: [
            "Event day",
            "Event list",
            "Event calendar",
            "Single event",
            "Event types",
          ],
        },
      ],
      Elements: [
        {
          title: "Classic",
          content: [
            "Accordion",
            "Buttons",
            "Clients",
            "Contact from",
            "Icon with text",
            "Image gallery",
          ],
        },
        {
          title: "Presentational",
          content: [
            "Booked calendar",
            "Event list",
            "Event list slider",
            "Blog list",
            "Portfolio list",
            "Shop list",
            "Team",
            "Testimonials",
          ],
        },
        {
          title: "Infographic",
          content: [
            "Counters",
            "Countdown",
            "Google maps",
            "Pie chart",
            "Progress bar",
            "Pricing tables",
            "Video button",
          ],
        },
        {
          title: "Typographic",
          content: [
            "Headings",
            "Columns",
            "Blockquote",
            "Custom font",
            "Dropcaps",
            "Section title",
            "Separators",
            "Highlights",
          ],
        },
      ],
    };
  },
  methods: {
    changetoggle() {
      this.togglesearch = !this.togglesearch;
    },
  },
};
</script>
<template lang="">
  <header class="w-100">
    <div
      class="container-fluid"
      v-bind:class="!togglesearch ? 'd-block' : 'd-none'"
    >
      <div class="row mx-5 h-100">
        <div class="col">
          <div class="navbar p-0 h-100">
            <div class="logo">
              <a href="#">
                <img src="/img/logo-img-01.png" alt="" class="logo" />
              </a>
            </div>
          </div>
        </div>
        <div class="col">
          <AppNavbar
            :menuItems="menuItems"
            :Elements="Elements"
            @change="changetoggle"
          ></AppNavbar>
        </div>
      </div>
    </div>
    <!-- searchbar -->
    <div
      class="container-fluid search_bar"
      v-bind:class="!togglesearch ? 'd-none' : 'd-block'"
    >
      <div class="row h-100">
        <div class="col">
          <div
            class="h-100 d-flex align-items-center justify-content-between p-4"
          >
            <input
              type="search"
              class="form-control"
              placeholder="Search..."
              aria-label="Search"
            />
            <div @click="changetoggle()">
              <i class="fa-solid fa-xmark fs-5 mx-2"></i>
            </div>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>
<style lang="scss">
header {
  position: absolute;
  z-index: 3;
}
.search_bar {
  height: 100px;
  background: white;
  input {
    border: none;
  }
  i:hover {
    cursor: pointer;
    color: #ff4612;
  }
}
</style>
