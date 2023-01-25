<script>
export default {
  data() {
    return {
      footerItems: [
        {
          title: "About",
          content: [
            "We created Everlead to effectively become the stepping stone towards meeting all your goals & achieving business success.",
          ],
        },
        {
          title: "Twitter",
          content: [
            `<div><i class="fa-brands fa-twitter"></i></div><div><a href="#">@UpTheIrons1978</a> did not find it, but created - <a href="https://t.co/joSV0jD3Yd">https://t.co/joSV0jD3Yd</a> Qi Blocks have 48 custom blocks for free</div>`,
            `<div><i class="fa-brands fa-twitter"></i></div><div><a href="#">@mrwebreviews</a> This could be caused by some 3rd party plugin, however, as we do not have enough information about se… <a href="https://t.co/YxmWae8sUVx">https://t.co/YxmWae8sUVx</a></div>`,
          ],
        },
        {
          title: "Important links",
          content: [
            "About me",
            "About us",
            "Language packs",
            "Become a coach",
            "Monthly events",
          ],
        },
        {
          title: "Contact me",
          content: [
            `<div><i class="fa-solid fa-location-dot"></i> 457 BigBlue Street, NY 10013</div>`,
            `<div><i class="fa-solid fa-phone"></i> (315) 5512-2579</div>`,
            `<div><i class="fa-regular fa-envelope"></i> everlead@qodeinteractive.com</div>`,
          ],
        },
      ],
    };
  },
};
</script>
<template lang="">
  <footer>
    <div class="container-fluid footer">
      <!-- footer 4 items -->
      <div class="row p-5">
        <div class="col m-2" v-for="(item, index) in footerItems">
          <!-- item title -->
          <p>
            {{ item.title }}
          </p>
          <div class="line"></div>
          <!-- item content -->
          <ul>
            <li v-html="item" v-for="(item, index) in item.content"></li>
          </ul>
        </div>
      </div>
    </div>
    <!-- copyright section -->
    <div class="container-fluid copyright">
      <div class="row">
        <div class="col">
          <a href="#">© 2019 Qode Interactive, All Rights Reserved</a>
        </div>
      </div>
    </div>
  </footer>
</template>
<style lang="scss">
@use "../styles/partials/variables" as *;
footer {
  .footer {
    background-color: #181515;
    height: 400px;
    color: white;
    p {
      font-family: "Libre Baskerville", serif;
      font-size: 19px;
      font-weight: 700;
    }
    .line {
      margin: 20px 0px;
      width: 32px;
      height: 1px;
      background-color: $orange-color;
    }
    ul {
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
          color: $orange-color;
          margin-right: 15px;
        }
      }
      li:hover {
        cursor: pointer;
      }
    }
  }
  .copyright {
    background-color: $orange-color;

    line-height: 50px;
    text-align: center;
    a {
      font-size: 13px;
      line-height: 22px;
      letter-spacing: 0.3px;
      color: white;
      text-decoration: none;
    }
    a:hover {
      cursor: pointer;
    }
  }
}
</style>
