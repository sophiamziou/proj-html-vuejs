<script>
export default {
  props: {
    menuItems: Array,
    Elements: Array,
  },
  data() {
    return {};
  },
};
</script>

<template lang="">
  <nav class="h-100">
    <ul class="nav nav-pills justify-content-end h-100">
      <li
        v-for="(item, index) in menuItems"
        :key="index"
        :class="item.active ? 'active' : ' '"
        class="nav-item mx-2"
      >
        <div class="dropdown_ h-100">
          <div class="dropbtn h-100">
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
                <div
                  class="col text-light w-100"
                  v-for="(item, index) in Elements"
                >
                  <div class="mx-5">
                    <p class="elem_title">
                      {{ item.title }}
                    </p>
                    <ul class="elem_list">
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
      <li class="nav-item mx-2">
        <div class="menuitem h-100 position-relative" @click="$emit('change')">
          <i
            class="fa-solid fa-magnifying-glass position-absolute top-50 start-50 translate-middle fs-5"
          ></i>
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
  cursor: pointer;
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

.dropdown_ {
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
  width: 900px;
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

.elem_title {
  font-family: "Libre Baskerville", serif;
  font-size: 14px;
  font-weight: 700;
}
.elem_list {
  color: grey;
  padding: 0;
  li {
    display: flex;
    list-style: none;
    margin: 8px 0;
    a {
      color: #ccc;
    }
    i {
      color: #ff4612;
      margin-right: 15px;
    }
  }
  li:hover {
    cursor: pointer;
    color: white;
  }
}
</style>
