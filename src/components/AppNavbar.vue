<script>
export default {
  props: {
    menuItems: Array,
  },
  data() {
    return {};
  },
};
</script>

<template lang="">
  <nav>
    <ul class="nav nav-pills">
      <li
        v-for="(item, index) in menuItems"
        :key="index"
        :class="item.active ? 'active' : ' '"
        class="nav-item mx-2"
      >
        <div class="dropdown_">
          <div class="dropbtn">
            <a
              :href="item.url"
              :class="item.active ? 'active' : ' '"
              class="menuitem"
            >
              {{ item.label }}
            </a>
          </div>
          <div class="dropdown_content">
            <a v-for="(item, index) in item.sublabel" :key="index" href="#">
              {{ item }}
            </a>
          </div>
        </div>
      </li>
      <li class="nav-item mx-2">
        <div class="dropdown_">
          <div class="dropbtn menuitem">ELEMENTS</div>
          <div class="dropdown_content right">
            <div class="container">
              <div class="row">
                <div class="col text-light" v-for="(item, index) in Elements">
                  <div>
                    <p>
                      {{ item.title }}
                    </p>
                    <ul>
                      <li
                        v-html="item"
                        v-for="(item, index) in item.content"
                      ></li>
                    </ul>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </li>
    </ul>
  </nav>
</template>
<style lang="scss">
.logo {
  width: 150px;
}
.menuitem {
  font-size: 15px;
  font-weight: 600;
  text-decoration: none;
  color: black;
  line-height: 50px;
}
.menuitem:hover {
  color: #ff4162;
}
.active {
  color: #ff4162;
}
.dropbtn {
  color: black;
  padding: 16px;
  font-size: 16px;
  border: none;
}

.dropdown {
  position: relative;
  display: inline-block;
}

.dropdown_content {
  display: none;
  position: absolute;
  min-width: 160px;
  box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
  z-index: 1;
  background-color: black;
  min-width: 250px;
  padding: 30px 15px;
}

.right {
  right: 0;
}
.dropdown_content a {
  color: grey;
  padding: 6px 16px;
  text-decoration: none;
  display: block;
}

.dropdown_content a:hover {
  color: white;
}

.dropdown_:hover .dropdown_content {
  display: block;
}
</style>
