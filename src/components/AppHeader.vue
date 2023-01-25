<script>
import AppNavbar from "./AppNavbar.vue";
export default {
  data() {
    return {
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
  components: {
    AppNavbar,
  },
};
</script>
<template lang="">
  <header class="container-fluid">
    <div class="row mx-5">
      <div class="col">
        <div class="navbar p-0">
          <div class="logo">
            <a href="#">
              <img src="/img/logo-img-01.png" alt="" class="logo" />
            </a>
          </div>
          <AppNavbar :menuItems="menuItems" :Elements="Elements"></AppNavbar>
        </div>
      </div>
    </div>
  </header>
</template>
<style lang="scss">
header {
  position: fixed;
  z-index: 3;
  background-color: white;
}
</style>
