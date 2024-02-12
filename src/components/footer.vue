<template>
  <div class="footer">
    <div class="goup"><button>بازگشت به بالا</button></div>
    <div class="service-footer">
      <div class="contact-info">
        <div class="address">
          <h3>پشتیبانی</h3>
          <p class="tel">
            <span>تلفنی: </span><a href="tel:\\03491002425">91002425-034</a>
            <span class="time">
              شنبه تا چهارشنبه 8 الی 21 - پنج شنبه 8 الی 20:30</span
            >
          </p>
          <p>ایمیل : info@mobit.ir</p>
        </div>
      </div>
      <div class="service-icon">
        <BoxIcon
          v-for="items in icon"
          :url="items.url"
          :caption="items.caption"
          size="footer"
          class="icon"
        />
      </div>
    </div>
    <div class="links">
      <div class="internal-links">
        <div class="column" v-for="link in links">
          <h3>{{ link.title }}</h3>
          <a href="" v-for="a in link.colLink">{{ a }}</a>
        </div>
      </div>
      <div class="social-links">
        <h2>با ما همراه باشید</h2>
        <div class="social">
          <div id="instagram">
            <a href="https://instagram.com"
              ><img src="/img/instagramIcon.webp"
            /></a>
          </div>
          <div id="aparat">
            <a href="https://aparat.com"><img src="/img/aparatIcon.webp" /></a>
          </div>
        </div>
      </div>
    </div>
    <TitlebarVue class="app-link" iscenter="false">
      <template v-slot:title
        ><span class="app-title">امکانات بیشتر در اپ مبیت</span></template
      >
      <template v-slot:showAll>
        <div class="apps">بازار</div>
        <div class="apps">مایکت</div>
        <div class="apps">اپ استور</div>
      </template>
    </TitlebarVue>
    <div class="meta-footer">
      <div class="discription">
        <h2>
          فروشگاه اینترنتی مبیت، خرید آسان کالای دیجیتال با مناسب ترین قیمت
        </h2>
        <p>
          فروشگاه اینترنتی مبیت از جمله عرضه‌کنندگان کالای دیجیتال در سراسر کشور
          است که انواع کالاهای دیجیتال از جمله گوشی موبایل، لپ تاپ، تبلت و لوازم
          جانبی گوشی را با قیمت مناسب و ضمانت اصالت کالا به فروش می‌رساند.
          فعالیت مبیت از سال 1393 به صورت رسمی آغاز شد و به لطف سالیان تجربه ما
          در زمینه فروش حضوری، توانستیم نیاز کاربران را به خوبی برآورده
        </p>
      </div>
      <div class="certificate">
        <div>
          <img src="/img/certificate/cert1.webp" />
        </div>
        <div>
          <img src="/img/certificate/cert2.webp" />
        </div>
        <div>
          <img src="/img/certificate/cert3.webp" />
        </div>
        <div>
          <img src="/img/certificate/cert4.webp" />
        </div>
      </div>
    </div>
    <div class="copyright">طراحی مجدد توسط امین آموزنده</div>
  </div>
</template>

<script setup>
import BoxIcon from "./BoxIcon.vue";
import TitlebarVue from "./Titlebar.vue";

const icon = [
  {
    url: "/img/serviceIcon/serIcon1.webp",
    caption: "ارسال سریع کالا",
  },
  {
    url: "/img/serviceIcon/serIcon2.webp",
    caption: "مهلت 7 روز بازگشت کالا",
  },
  {
    url: "/img/serviceIcon/serIcon3.webp",
    caption: "پشتیبانی تلفنی",
  },
  {
    url: "/img/serviceIcon/serIcon4.webp",
    caption: "تضمین اصالت کالا",
  },
];
const links = [
  {
    title: "با مبیت",
    colLink: [
      "درباره مبیت",
      "تماس با مبیت",
      "تماس با مدیریت",
      "فرصت شغلی",
      "فروش عمده همکار",
      "شعب حضوری",
    ],
  },
  {
    title: "راهنمای خرید",
    colLink: [
      "روش پرداخت",
      "روش ارسال کالا",
      "روش بازگشت وجه",
      "ضمانت اصالت کالا",
    ],
  },
  {
    title: "خدمات مشتریان",
    colLink: [
      "درباره مبیت",
      "تماس با مبیت",
      "تماس با مدیریت",
      "فرصت شغلی",
      "فروش عمده همکار",
      "شعب حضوری",
    ],
  },
  {
    title: "قیمت گوشی",
    colLink: [
      "درباره مبیت",
      "تماس با مبیت",
      "تماس با مدیریت",
      "فرصت شغلی",
      "فروش عمده همکار",
      "شعب حضوری",
    ],
  },
];
</script>

<style scoped>
.footer {
  display: flex;
  flex-direction: column;
  margin-top: 2rem;
  font-family: iranfaNum-bold;
  font-size: 0.8rem;
}
.h3 {
  font-size: 1rem;
}
.goup {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
.goup button {
  border: none;
  border-radius: 10px 10px 0 0;
  background-color: var(--color-place-holder);
  padding: 0.5rem 1.4rem;
  font-family: iran-bold;
  font-size: 0.8rem;
}
.service-footer {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  background-color: var(--color-place-holder);
  border-radius: 10px;
  padding: 1.2rem 1.5rem;
}
.contact-info {
  display: flex;
  flex-direction: column;
}
.address {
  display: flex;
  flex-direction: column;
}
.address p {
  margin-top: 1.2rem;
}

.tel .time {
  margin-right: 0.5rem;
  border-right: 1px solid var(--color-place-holder2);
  padding-right: 1rem;
}

.service-icon {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
}

.service-icon .icon {
  height: 148px;
  width: 148px;
}
.apps {
  padding: 0.5rem 2rem;
  background-color: var(--color-text-light);
  border-radius: 10px;
  margin: 0.5rem;
}
.links {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  margin-top: 1rem;
}
.internal-links {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  width: 50%;
}
.column {
  display: flex;
  flex-direction: column;
}
.column a {
  margin-top: 1rem;
  opacity: 0.6;
}
.social-links {
  display: flex;
  flex-direction: row;
  justify-content: end;
}
.social-links h2 {
  padding-top: 0.5rem;
}
.social {
  display: flex;
  align-items: flex-start;
}
#instagram {
  opacity: 0.2;
}
#instagram:hover {
  opacity: 1;
}
#aparat {
  opacity: 0.2;
}
#aparat:hover {
  opacity: 1;
}
.meta-footer {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  border-bottom: 1px solid var(--color-place-holder2);
  margin-bottom: 1.5rem;
  padding-bottom: 2rem;
}
.discription {
  display: flex;
  flex-direction: column;
  width: 60%;
  line-height: 1.5rem;
}
.discription p {
  padding-top: 1.2rem;
  opacity: 0.6;
}
.app-title {
  color: blue;
}
.certificate {
  display: flex;
  flex-direction: row-reverse;
  justify-content: space-evenly;
}
.certificate img {
  height: 100px;
  width: 100px;
}
.copyright {
  margin-bottom: 2rem;
}
@media (max-width: 1024px) {
  .service-footer {
    flex-direction: column-reverse;
  }
  .service-icon {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
  }
  .service-icon .icon {
    width: 100%;
  }
  .links {
    flex-direction: column;
  }
  .social-links {
    justify-content: space-between;
  }
  .meta-footer {
    flex-direction: column;
  }
  .meta-footer .discription {
    width: 100%;
    margin-bottom: 1rem;
  }
  .app-link {
    flex-direction: column;
    height: auto;
  }
  .internal-links {
    width: 100%;
  }
}
@media (max-width: 360px) {
  .links {
    overflow-x: auto;
    position: relative;
  }
  .internal-links {
    width: max-content;
  }
  .internal-links .column {
    margin-left: 1.5rem;
  }

  .certificate {
    flex-wrap: wrap;
  }
}
</style>
