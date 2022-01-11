<template>
  <div class="home">
    <svg
      xmlns="http://www.w3.org/2000/svg"
      class="goo"
      version="1.1"
      width="100%"
    >
      <defs>
        <filter id="goo">
          <feGaussianBlur
            in="SourceGraphic"
            stdDeviation="6"
            result="blur"
          ></feGaussianBlur>
          <feColorMatrix
            in="blur"
            mode="matrix"
            values="1 0 0 0 0  0 1 0 0 0  0 0 1 0 0  0 0 0 35 -15"
            result="goo"
          ></feColorMatrix>
          <feComposite
            in="SourceGraphic"
            in2="goo"
            operator="atop"
          ></feComposite>
        </filter>
      </defs>
    </svg>

    <div ref="cursor" class="cursor"></div>
    <main>
      <header class="sticky-header">
        <div class="logo-wrapper" ref="logoWrapper">
          <a>
            <img
              class="header-logo"
              src="https://global-uploads.webflow.com/5c9c9c646cf0969b319f264f/5d10db9372c981e229f12d3d_de-logotype-vert.svg"
            />
            <img
              class="header-logo"
              src="https://global-uploads.webflow.com/5c9c9c646cf0969b319f264f/5d10db9372c981e229f12d3d_de-logotype-vert.svg"
            />
          </a>
        </div>
        <div class="cart-text" ref="cartText">
          <div>
            <p>Cart</p>
            <p>Cart</p>
          </div>
          <a class="number-of-items">0</a>
        </div>
        <div class="header-menu">
          <a href=""
            ><div>SHOP</div>
            <div>SHOP</div></a
          >
          <a href=""
            ><div>COLLECTIONS</div>
            <div>COLLECTIONS</div></a
          >
          <a href=""
            ><div>ABOUT</div>
            <div>ABOUT</div></a
          >
        </div>
      </header>
      <div class="ink-mode">
        <p class="ink-mode-text">Ink mode</p>
      </div>
      <div class="first-part-wrapper">
        <div class="main-title" ref="mainTitle">
          <div><h1>SPRING,</h1></div>
          <div><h1>SUMMER</h1></div>
          <div><h3>COLL. 2021</h3></div>
        </div>
        <div class="brand-image" ref="brandImage">
          <div class="mark">
            <img
              src="https://global-uploads.webflow.com/5c9c9c646cf0969b319f264f/5d09026ed5102a6910070111_scotch-tape.svg"
              alt=""
              class="s-tape"
            />
          </div>
          <span>
            <div>
              <img
                src="https://global-uploads.webflow.com/5c9c9c646cf0969b319f264f/5ede27e188219c6c4ab2af6b_man-default.jpg"
                ref="image1"
              />
            </div>

            <div>
              <h3>(01) <span>MAN</span></h3>
            </div>
          </span>
          <span>
            <div>
              <img
                src="https://global-uploads.webflow.com/5c9c9c646cf0969b319f264f/5ede29ef88219c8178b2be22_women-default.jpg"
                ref="image2"
              />
            </div>

            <div>
              <h3>(02) <span>WMNS</span></h3>
            </div>
          </span>
        </div>
        <div class="explore">
          <h3>EXPLORE</h3>
          <a class="explore-button">
            <img
              src="https://global-uploads.webflow.com/5c9c9c646cf0969b319f264f/5d14818767ac37ac193eccf4_circle-container.svg"
              alt="circle"
            />
            <img
              src="https://global-uploads.webflow.com/5c9c9c646cf0969b319f264f/5d24aa633c6cae18850994a2_arrow.svg"
              alt="arrow-right"
            />
          </a>
        </div>
      </div>
      <div class="warning-message-wrapper">
        <div class="band">
          <div>
            <h3 v-for="index in 6" :key="index">
              DO NOT SCROLL
              <div>.</div>
              DEPLACE SHOP
              <div>.</div>
            </h3>
          </div>
        </div>
      </div>
      <div class="second-part-wrapper">
        <div class="second-part-text" ref="aboutUs">
          <div><h3>WHO WE ARE</h3></div>
          <div><h2>An independent brand of</h2></div>
          <div><h2>urban trekking shoes and accessories</h2></div>
          <div><h2>that comes from a convergence of</h2></div>
          <div><h2>arts and personalities</h2></div>
        </div>
        <div class="product-list" ref="productList">
          <div class="productSlider">
            <div class="product">
              <div class="product-item-wrapper">
                <img
                  alt="item"
                  src="https://global-uploads.webflow.com/5d07507a85189203b7002a95/5ed0ce1058516c6883c51225_du-sand-side.jpg"
                  sizes="(max-width: 479px) 48vw, (max-width: 767px) 19vw, (max-width: 991px) 27vw, 23vw"
                  srcset="
                    https://global-uploads.webflow.com/5d07507a85189203b7002a95/5ed0ce1058516c6883c51225_du-sand-side-p-500.jpeg   500w,
                    https://global-uploads.webflow.com/5d07507a85189203b7002a95/5ed0ce1058516c6883c51225_du-sand-side-p-800.jpeg   800w,
                    https://global-uploads.webflow.com/5d07507a85189203b7002a95/5ed0ce1058516c6883c51225_du-sand-side-p-1080.jpeg 1080w,
                    https://global-uploads.webflow.com/5d07507a85189203b7002a95/5ed0ce1058516c6883c51225_du-sand-side.jpg         1600w
                  "
                  class="item-img"
                />
              </div>
              <div class="product-description">
                <img
                  src="https://global-uploads.webflow.com/5c9c9c646cf0969b319f264f/5ed0ddbec534bd9d113f6188_unisex-label.svg"
                  alt=""
                  class="product-label"
                />
                <p class="item-season">SS/20</p>
                <h2>DURAN</h2>
                <p class="price">€ 240 EUR</p>
                <p class="sold-price">€ 144 EUR</p>
              </div>
            </div>
            <div class="product">
              <div class="product-item-wrapper">
                <img
                  alt="item"
                  src="https://global-uploads.webflow.com/5d07507a85189203b7002a95/5ed0cf7411a8b0b111096fd5_tc-black-side.jpg"
                  sizes="(max-width: 479px) 48vw, (max-width: 767px) 19vw, (max-width: 991px) 27vw, 23vw"
                  srcset="
                    https://global-uploads.webflow.com/5d07507a85189203b7002a95/5ed0cf7411a8b0b111096fd5_tc-black-side-p-500.jpeg   500w,
                    https://global-uploads.webflow.com/5d07507a85189203b7002a95/5ed0cf7411a8b0b111096fd5_tc-black-side-p-800.jpeg   800w,
                    https://global-uploads.webflow.com/5d07507a85189203b7002a95/5ed0cf7411a8b0b111096fd5_tc-black-side-p-1080.jpeg 1080w,
                    https://global-uploads.webflow.com/5d07507a85189203b7002a95/5ed0cf7411a8b0b111096fd5_tc-black-side.jpg         1600w
                  "
                  class="item-img"
                />
              </div>
              <div class="product-description">
                <img
                  src="https://global-uploads.webflow.com/5c9c9c646cf0969b319f264f/5ed0ddbec534bd9d113f6188_unisex-label.svg"
                  alt=""
                  class="product-label"
                />
                <p class="item-season">SS/20</p>
                <h2>THE CODE</h2>
                <p class="price">€ 240 EUR</p>
                <p class="sold-price">€ 144 EUR</p>
              </div>
            </div>
            <div class="product">
              <div class="product-item-wrapper">
                <img
                  alt="item"
                  src="https://global-uploads.webflow.com/5d07507a85189203b7002a95/5ecf8747b314ba36a789e3c4_ct-army-side.jpg"
                  sizes="(max-width: 479px) 48vw, (max-width: 767px) 19vw, (max-width: 991px) 27vw, 23vw"
                  srcset="
                    https://global-uploads.webflow.com/5d07507a85189203b7002a95/5ecf8747b314ba36a789e3c4_ct-army-side-p-500.jpeg   500w,
                    https://global-uploads.webflow.com/5d07507a85189203b7002a95/5ecf8747b314ba36a789e3c4_ct-army-side-p-800.jpeg   800w,
                    https://global-uploads.webflow.com/5d07507a85189203b7002a95/5ecf8747b314ba36a789e3c4_ct-army-side-p-1080.jpeg 1080w,
                    https://global-uploads.webflow.com/5d07507a85189203b7002a95/5ecf8747b314ba36a789e3c4_ct-army-side.jpg         1600w
                  "
                  class="item-img"
                />
              </div>
              <div class="product-description">
                <img
                  src="https://global-uploads.webflow.com/5c9c9c646cf0969b319f264f/5ed0ddbec534bd9d113f6188_unisex-label.svg"
                  alt=""
                  class="product-label"
                />
                <p class="item-season">SS/20</p>
                <h2>CACTUS</h2>
                <p class="price">€ 300 EUR</p>
                <p class="sold-price">€ 180 EUR</p>
              </div>
            </div>
            <div class="product">
              <div class="product-item-wrapper">
                <img
                  alt="item"
                  src="https://global-uploads.webflow.com/5d07507a85189203b7002a95/5ed0d5b0a20c8f34cdca447c_te-sand-side.jpg"
                  sizes="(max-width: 479px) 48vw, (max-width: 767px) 19vw, (max-width: 991px) 27vw, 23vw"
                  srcset="
                    https://global-uploads.webflow.com/5d07507a85189203b7002a95/5ed0d5b0a20c8f34cdca447c_te-sand-side-p-500.jpeg  500w,
                    https://global-uploads.webflow.com/5d07507a85189203b7002a95/5ed0d5b0a20c8f34cdca447c_te-sand-side-p-800.jpeg  800w,
                    https://global-uploads.webflow.com/5d07507a85189203b7002a95/5ed0d5b0a20c8f34cdca447c_te-sand-side.jpg        1600w
                  "
                  class="item-img"
                />
              </div>
              <div class="product-description">
                <img
                  src="https://global-uploads.webflow.com/5c9c9c646cf0969b319f264f/5ed0ddbec534bd9d113f6188_unisex-label.svg"
                  alt=""
                  class="product-label"
                />
                <p class="item-season">SS/20</p>
                <h2>THE EYE</h2>
                <p class="price">€ 240 EUR</p>
                <p class="sold-price">€ 144 EUR</p>
              </div>
            </div>
            <div class="product">
              <div class="product-item-wrapper">
                <img
                  alt="item"
                  src="https://global-uploads.webflow.com/5d07507a85189203b7002a95/5ed0ca93411f13ef43fe2ef2_ca-black-side.jpg"
                  sizes="(max-width: 479px) 48vw, (max-width: 767px) 19vw, (max-width: 991px) 27vw, 23vw"
                  srcset="
                    https://global-uploads.webflow.com/5d07507a85189203b7002a95/5ed0ca93411f13ef43fe2ef2_ca-black-side-p-500.jpeg   500w,
                    https://global-uploads.webflow.com/5d07507a85189203b7002a95/5ed0ca93411f13ef43fe2ef2_ca-black-side-p-800.jpeg   800w,
                    https://global-uploads.webflow.com/5d07507a85189203b7002a95/5ed0ca93411f13ef43fe2ef2_ca-black-side-p-1080.jpeg 1080w,
                    https://global-uploads.webflow.com/5d07507a85189203b7002a95/5ed0ca93411f13ef43fe2ef2_ca-black-side.jpg         1600w
                  "
                  class="item-img"
                />
              </div>
              <div class="product-description">
                <img
                  src="https://global-uploads.webflow.com/5c9c9c646cf0969b319f264f/5ed0ddbec534bd9d113f6188_unisex-label.svg"
                  alt=""
                  class="product-label"
                />
                <p class="item-season">SS/20</p>
                <h2>CARNERA</h2>
                <p class="price">€ 240 EUR</p>
                <p class="sold-price">€ 144 EUR</p>
              </div>
            </div>
          </div>
        </div>
        <div class="explore">
          <h3>SHOP ALL</h3>
          <a class="explore-button">
            <img
              src="https://global-uploads.webflow.com/5c9c9c646cf0969b319f264f/5d14818767ac37ac193eccf4_circle-container.svg"
              alt="circle"
            />
            <img
              src="https://global-uploads.webflow.com/5c9c9c646cf0969b319f264f/5d24aa633c6cae18850994a2_arrow.svg"
              alt="arrow-right"
            />
          </a>
        </div>
      </div>
      <div class="third-part-wrapper">
        <div class="testimonials">
          <div class="first-part" ref="reviewsFirstPart">
            <img
              src="https://global-uploads.webflow.com/5c9c9c646cf0969b319f264f/5d0b92e20369a4438cd54272_virgolette.svg"
              alt="mark"
            />
            <div>
              <div><h3>William Gibson</h3></div>
              <div><h3>JAMIE K. COTTEN</h3></div>
            </div>
          </div>
          <div class="second-part">
            <div class="reviews" ref="reviewsSecondPart">
              <div>
                <p>
                  Good things come to those who wait – Déplacé Maison is what
                  has been missing in the modern fashion industry for years. Buy
                  a shoe of high quality and design it finally happened.
                </p>
              </div>
              <div>
                <p>
                  Déplacé Maison is a convincer for anticipation. The urban
                  trekking as nevers seen before. An exceptional product that
                  has no equal alongside a great team represent the brand
                  professionally.
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
      <footer class="footer-wrapper">
        <div class="footer-grid">
          <div class="a">
            <h4>Subscribe to newsletter</h4>
            <img
              src="https://global-uploads.webflow.com/5c9c9c646cf0969b319f264f/5d2dc19a2be6baa7f9e25b8c_newsletter-face.svg"
              class="newsletter"
            />
          </div>
          <div class="b">
            <h4>Subscribe to our newsletter</h4>
            <div class="input-wrapper">
              <input type="email" placeholder="email address" /><input
                type="button"
                value="Submit"
              />
            </div>
          </div>
          <div class="c">
            <div class="upper-text">
              <h5>info</h5>
              <div>
                <h2>faq</h2>
                <h2>faq</h2>
              </div>
              <div>
                <h2>returns</h2>
                <h2>returns</h2>
              </div>
              <div>
                <h2>contact</h2>
                <h2>contact</h2>
              </div>
            </div>
            <div class="lower-text">
              <h5>credits</h5>
            </div>
          </div>
          <div class="d">
            <div class="upper-text">
              <h5>policy</h5>
              <div>
                <h2>terms</h2>
                <h2>terms</h2>
              </div>
              <div>
                <h2>privacy</h2>
                <h2>privacy</h2>
              </div>
              <div>
                <h2>cookie</h2>
                <h2>cookie</h2>
              </div>
            </div>
            <div class="lower-text">
              <h5>© 2020 déplacé maison.</h5>
            </div>
          </div>
          <div class="e">
            <span class="to-the-top"
              ><a class="explore-button">
                <img
                  src="https://global-uploads.webflow.com/5c9c9c646cf0969b319f264f/5d14818767ac37ac193eccf4_circle-container.svg"
                  alt="circle"
                />
                <img
                  src="https://global-uploads.webflow.com/5c9c9c646cf0969b319f264f/5d24aa633c6cae18850994a2_arrow.svg"
                  alt="arrow-right"
                /> </a
            ></span>

            <div class="social-icon">
              <img
                src="https://global-uploads.webflow.com/5c9c9c646cf0969b319f264f/5d303c388e44eb6941b16af5_facebook.svg"
                width="16"
                alt=""
                class="f-social-icon"
              />
              <img
                src="https://global-uploads.webflow.com/5c9c9c646cf0969b319f264f/5d303c3985ef61f5a55c8a45_instagram.svg"
                alt=""
                class="f-social-icon"
              />
            </div>
          </div>
        </div>
      </footer>
    </main>
  </div>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      elements: [],
      currentTestimonials: 0,
    };
  },
  mounted() {
    this.gooeyCursor();
    this.initAnimation();
    document.addEventListener("scroll", this.animateOnViewportAppearance);
    document.addEventListener("scroll", this.zoomScrollBrandImage);
    this.dragShop();
    setInterval(() => {
      this.alternateTestimonials();
    }, 5000);
  },
  methods: {
    gooeyCursor() {
      const TAIL_LENGTH = 20;

      const cursor = document.querySelector(".cursor");

      let mouseX = 0;
      let mouseY = 0;

      let cursorCircles;
      let cursorHistory = Array(TAIL_LENGTH).fill({
        x: 0,
        y: 0,
      });

      function onMouseMove(event) {
        mouseX = event.clientX;
        mouseY = event.clientY;
      }

      function initCursor() {
        for (let i = 0; i < TAIL_LENGTH; i++) {
          let div = document.createElement("div");
          div.classList.add("cursor-circle");
          cursor.append(div);
        }
        cursorCircles = Array.from(document.querySelectorAll(".cursor-circle"));
      }

      function updateCursor() {
        cursorHistory.shift();
        cursorHistory.push({
          x: mouseX,
          y: mouseY,
        });

        for (let i = 0; i < TAIL_LENGTH; i++) {
          let current = cursorHistory[i];
          let next = cursorHistory[i + 1] || cursorHistory[TAIL_LENGTH - 1];

          let xDiff = next.x - current.x;
          let yDiff = next.y - current.y;

          current.x += xDiff * 0.35;
          current.y += yDiff * 0.35;
          cursorCircles[i].style.transform = `translate(${current.x}px, ${
            current.y
          }px) scale(${i / TAIL_LENGTH})`;
        }
        requestAnimationFrame(updateCursor);
      }

      document.addEventListener("mousemove", onMouseMove, false);

      initCursor();
      updateCursor();
    },
    initAnimation() {
      this.elements.push(
        this.$refs.mainTitle,
        this.$refs.logoWrapper,
        this.$refs.cartText,
        this.$refs.brandImage
      );
      this.animateAfterLoading();
    },
    animateAfterLoading() {
      let elements = this.elements;
      for (let i = 0; i < elements.length; i++) {
        let eclass = elements[i].className;
        if (eclass === "main-title") {
          elements[i].children[0].children[0].classList.add("title-animate");
          elements[i].children[1].children[0].classList.add("title-animate");
          elements[i].children[2].children[0].classList.add("title-animate");
        }
        if (eclass === "logo-wrapper") {
          elements[i].children[0].children[0].classList.add(
            "header-logo-animate"
          );
        }
        if (eclass === "cart-text") {
          elements[i].children[0].children[0].classList.add(
            "cart-text-animate"
          );
        }
        if (eclass === "brand-image") {
          elements[i].children[1].classList.add("brand-image-animate");
          elements[i].children[2].classList.add("brand-image-animate");
          setTimeout(() => {
            elements[i].children[0].children[0].classList.add("mark-animate");
          }, 1000);
        }
      }
      this.elements = [];
      this.elements.push(this.$refs.aboutUs, this.$refs.productList);
      this.animateOnViewportAppearance();
    },
    animateOnViewportAppearance() {
      let elements = this.elements;

      for (let i = 0; i < elements.length; i++) {
        if (
          window.pageYOffset >
            window.innerHeight + window.innerHeight * (2 / 3) &&
          elements[i].className === "second-part-text"
        ) {
          console.log("text in viewport");
          for (let j = 0; j < 5; j++) {
            elements[i].children[j].children[0].classList.add(
              "second-part-enter-animate"
            );
          }
        } else if (
          window.pageYOffset >
            window.innerHeight * 1.5 + window.innerHeight * (2 / 3) &&
          elements[i].className === "product-list"
        ) {
          elements[i].classList.add("product-list-animate");
          document.removeEventListener(
            "scroll",
            this.animateOnViewportAppearance
          );
        }
      }
    },
    zoomScrollBrandImage() {
      console.log(window.pageYOffset);
      let image1 = this.$refs.image1;
      let image2 = this.$refs.image2;
      let scale = 1;
      if (
        window.pageYOffset > 0 &&
        window.pageYOffset <= window.innerHeight + window.innerHeight * (2 / 3)
      ) {
        if (window.pageYOffset % 100 === 0) {
          let offset =
            window.pageYOffset.toString().length === 3
              ? window.pageYOffset.toString().substring(0, 1)
              : window.pageYOffset.toString().substring(0, 2);
          scale += 0.005 * offset;
          image1.style.transform = `scale(${scale})`;
          image2.style.transform = `scale(${scale})`;
        }
      }
    },
    alternateTestimonials() {
      let firstPart = this.$refs.reviewsFirstPart;
      let secondPart = this.$refs.reviewsSecondPart;
      let current = this.currentTestimonials;

      try {
        if (current === 0) {
          if (
            firstPart.children[1].children[0].children[0].classList.contains(
              "testimonials-animate-down-first"
            )
          ) {
            firstPart.children[1].children[0].children[0].classList.remove(
              "testimonials-animate-down-first"
            );
            firstPart.children[1].children[1].children[0].classList.remove(
              "testimonials-animate-down-second"
            );
            secondPart.children[0].classList.remove(
              "testimonials-animate-down-second-text"
            );
            secondPart.children[1].classList.remove(
              "testimonials-animate-down-second-text"
            );
          }
          firstPart.children[1].children[0].children[0].classList.add(
            "testimonials-animate-up-first"
          );
          firstPart.children[1].children[1].children[0].classList.add(
            "testimonials-animate-up-second"
          );
          secondPart.children[0].classList.add("testimonials-animate-up-second-text");
          secondPart.children[1].classList.add(
            "testimonials-animate-up-second-text"
          );
          this.currentTestimonials = 1;
          return;
        } else {
          if (
            firstPart.children[1].children[0].children[0].classList.contains(
              "testimonials-animate-up-first"
            )
          ) {
            firstPart.children[1].children[0].children[0].classList.remove(
              "testimonials-animate-up-first"
            );
            firstPart.children[1].children[1].children[0].classList.remove(
              "testimonials-animate-up-second"
            );
            secondPart.children[0].classList.remove(
              "testimonials-animate-up-second-text"
            );
            secondPart.children[1].classList.remove(
              "testimonials-animate-up-second-text"
            );
          }
          firstPart.children[1].children[0].children[0].classList.add(
            "testimonials-animate-down-first"
          );
          firstPart.children[1].children[1].children[0].classList.add(
            "testimonials-animate-down-second"
          );
          secondPart.children[0].classList.add(
            "testimonials-animate-down-second-text"
          );
          secondPart.children[1].classList.add(
            "testimonials-animate-down-second-text"
          );
          this.currentTestimonials = 0;
          return;
        }
      } catch (err) {
        console.error(err.message);
      }
    },
    dragShop() {
      let pressed = false;
      let startX = 0;
      let x = 0;
      let offset;
      let list = this.$refs.productList;
      let listSlider = list.children[0];

      this.$refs.productList.addEventListener("mousedown", function (e) {
        e.preventDefault();
        pressed = true;
        startX = e.offsetX - listSlider.offsetLeft;
        listSlider.style.cursor = "grabbing";
      });
      this.$refs.productList.addEventListener("mouseenter", (e) => {
        e.preventDefault();
        listSlider.style.cursor = "grab";
      });
      this.$refs.productList.addEventListener("mouseup", () => {
        listSlider.style.cursor = "grab";
      });
      window.addEventListener("mouseup", function () {
        pressed = false;
      });
      this.$refs.productList.addEventListener("mousemove", (e) => {
        if (!pressed) return;
        e.preventDefault();
        x = e.offsetX;
        offset = x - startX;
        console.log(offset);
        listSlider.style.left = offset + "px";
        setTimeout(() => {}, 300);
        checkBoundary();
      });
      let checkBoundary = () => {
        let inner = listSlider.getBoundingClientRect();
        let outer = list.getBoundingClientRect();

        if (inner.left > window.innerWidth / 3) {
          listSlider.style.transition = "left 0.5s ease-in";
          listSlider.style.left = "0";
          setTimeout(() => {
            listSlider.style.transition = "unset";
          }, 600);
        } else if (inner.right < window.innerWidth / 2) {
          listSlider.style.transition = "left 0.5s ease-in";
          listSlider.style.left = `-${inner.width - outer.width}px`;
          setTimeout(() => {
            listSlider.style.transition = "unset";
          }, 600);
        }
      };
      checkBoundary();
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import "Home.css";
@import "Home_Responsive.css";
</style>
