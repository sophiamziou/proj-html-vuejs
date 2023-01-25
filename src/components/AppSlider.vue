<script>
export default {
  data() {
    return {
      auto_play: null,
      activeImage: 0,
      slides: [
        {
          image: "/img/h1-rev-img-01.jpg",
          title: "We are Everlead",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Illum obcaecati aut, numquam natus quisquam harum est quidem soluta commodi",
        },
        {
          image: "/img/rev-slider-main-home-img-02.png",
          title: "Our Team",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Illum obcaecati aut, numquam natus quisquam harum est quidem soluta commodi",
        },
        {
          image: "/img/rev-slider-main-home-img-03.jpg",
          title: "Help you achive anything",
        },
      ],
    };
  },
  methods: {
    changeImage(index) {
      this.activeImage = index;
    },
    next() {
      if (this.activeImage < this.slides.length - 1) {
        this.activeImage++;
      } else {
        this.activeImage = 0;
      }
    },
    prev() {
      if (this.activeImage > 0) {
        this.activeImage--;
      } else {
        this.activeImage = this.slides.length - 1;
      }
    },
    autoPlay() {
      this.auto_play = setInterval(() => {
        this.next();
      }, 3000);
    },
  },
  created() {
    this.autoPlay();
  },
};
</script>
<template lang="">
  <div class="container-fluid p-0">
    <div class="slider-wrapper" tabindex="0">
      <div class="item">
        <!-- <img src="/public/img/h1-blog-img-01.jpg" alt="" /> -->
        <img v-bind:src="slides[activeImage].image" v-bind:alt="slides.title" />
        <div class="text">
          <h1 class="my-4">{{ slides[activeImage].title }}</h1>
          <p class="fs-4">
            {{ slides[activeImage].text }}
          </p>
          <button>READ MORE</button>
          <button class="orange">PURCHASE</button>
        </div>
      </div>
      <div class="prev" @click="prev">&#8592;</div>
      <div class="next" @click="next">&#8594;</div>
    </div>
  </div>
</template>
<style lang="scss">
.container {
  display: flex;
  justify-content: center;
  align-items: center;
}

.item {
  float: left;
  width: 100%;
  height: 100vh;
  position: relative;
}

.item img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.item .text {
  position: absolute;
  top: 45%;
  left: 30%;
  transform: translate(-50%, -50%);
  width: 600px;
  text-align: left;
  color: black;
  button {
    margin: 20px;
    height: 50px;
    width: 150px;
    border: none;
    color: black;
    background-color: white;
    font-weight: 700;
  }
  .orange {
    color: white;
    background-color: #ff4612;
  }
}

.prev,
.next {
  font-size: 30px;
  margin: 10px 0;
  position: absolute;
  top: 45%;
  transform: translate(-50%, -50%);
  cursor: pointer;
  z-index: 2;
}

.prev {
  left: 5%;
}

.next {
  right: 5%;
}

h1 {
  font-family: "Libre Baskerville", serif;
  font-size: 70px;
  font-weight: 700;
}
</style>
