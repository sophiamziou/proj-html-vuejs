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
            "@UpTheIrons1978 did not find it, but created - https://t.co/joSV0jD3Yd Qi Blocks have 48 custom blocks for free",
            "@mrwebreviews This could be caused by some 3rd party plugin, however, as we do not have enough information about se… https://t.co/YxmWae8sUV",
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
            " 457 BigBlue Street, NY 10013",
            "(315) 5512-2579 ",
            "everlead@qodeinteractive.com",
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
      <div class="row">
        <div class="col my-5" v-for="(item, index) in footerItems">
          <p>
            {{ item.title }}
          </p>
          <ul>
            <li v-for="(item, index) in item.content">
              {{ item }}
            </li>
          </ul>
        </div>
      </div>
    </div>
    <div class="container-fluid copyright">
      <div class="row">
        <div class="col">
          <a href="#">© 2019 Qode Interactive, All Rights Reserved</a>
          <a href="#"></a>
        </div>
      </div>
    </div>
  </footer>
</template>
<style lang="scss">
footer {
  .footer {
    background-color: #181515;
    height: 400px;
    color: white;
    p {
      font-family: "Libre Baskerville", serif;
      font-size: 19px;
      font-weight: 700;
      padding: 20px 0px;
      border-bottom: 1px solid #ff4612;
    }
    ul {
      color: grey;
      padding: 0;
      li {
        list-style: none;
        margin: 8px 0;
      }
      li:hover {
        color: white;
        cursor: pointer;
      }
    }
  }
  .copyright {
    background-color: #ff4612;

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
