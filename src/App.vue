<template>
  <div id="app">
    <main class="main">
      <div class="main__row">
        <a class="main__logo" href="/">
          <img src="@/assets/logo.png" alt="ONE VISION" />
        </a>
        <div>
          <div class="main__row-mobile">
            <div class="container">
              <div class="main__row-mobile--inner">
                <button
                  @click="mobileNavVisible = !mobileNavVisible"
                  class="main__nav-dropdown"
                >
                  <p>Real Time Cashflow</p>
                  <div
                    class="dropdown-arrow"
                    :class="{ 'is-active': mobileNavVisible }"
                  >
                    <svg
                      width="12"
                      height="8"
                      viewBox="0 0 12 8"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <path
                        fill-rule="evenodd"
                        clip-rule="evenodd"
                        d="M5.65664 4.24242L1.41421 0L0 1.41421L4.24242 5.65664L4.24221 5.65685L5.65642 7.07107L5.65664 7.07085L5.65685 7.07107L7.07107 5.65685L7.07085 5.65664L11.3133 1.41421L9.89906 0L5.65664 4.24242Z"
                      />
                    </svg>
                  </div>
                </button>
                <div class="pos-relative">
                  <button
                    v-if="!mobileNavVisible"
                    @click="settingsVisible = !settingsVisible"
                    class="main__row-mobile--settings main__btn main__elem"
                  >
                    <svg
                      class="main__settings-icon"
                      width="25"
                      height="24"
                      viewBox="0 0 25 24"
                      fill="none"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <path
                        fill-rule="evenodd"
                        clip-rule="evenodd"
                        d="M8.94421 23.9509L6.88139 23.1896C6.55574 23.069 6.3454 22.754 6.35821 22.4081L6.45111 19.8626L5.48696 19.0426L3.04297 19.5765C2.70023 19.6512 2.34896 19.4943 2.17599 19.19L1.07625 17.2617C0.905412 16.9627 0.944917 16.589 1.17341 16.3317L2.85932 14.4419L2.63831 13.1734L0.421738 11.984C0.118508 11.8206 -0.0469871 11.48 0.0117371 11.1405L0.39291 8.94849C0.452702 8.60575 0.726036 8.34096 1.07091 8.29185L3.548 7.94271L4.18222 6.83015L3.23516 4.47051C3.10703 4.15126 3.19779 3.78504 3.46045 3.56188L5.14316 2.13222C5.41009 1.9048 5.79553 1.87811 6.09129 2.06602L8.20963 3.41347L9.38624 2.97891L10.1561 0.558413C10.2628 0.225286 10.5714 0 10.9205 0H13.1179C13.466 0 13.7745 0.225285 13.8813 0.557344L14.6522 2.97785L15.8277 3.41134L17.945 2.06388C18.2408 1.87597 18.6262 1.90266 18.8931 2.13008L20.5769 3.56082C20.8396 3.78397 20.9303 4.14913 20.8022 4.46944L19.8552 6.82908L20.4904 7.94271L22.9665 8.28971C23.3103 8.33883 23.5847 8.60362 23.6445 8.94635L24.0267 11.1384C24.0854 11.4779 23.9199 11.8185 23.6167 11.9819L21.4001 13.1713L21.1802 14.4397L22.865 16.3285C23.0946 16.5848 23.1341 16.9595 22.9643 17.2585L21.8646 19.1878C21.6906 19.4921 21.3393 19.6491 20.9976 19.5744L18.5547 19.0416L17.5895 19.8626L17.6824 22.407C17.6952 22.7529 17.4848 23.0679 17.1603 23.1886L15.0964 23.9509C14.7664 24.0716 14.3959 23.9648 14.1824 23.6861L12.646 21.6831L11.3946 21.6842L9.85711 23.6861C9.64356 23.9648 9.27307 24.0716 8.94421 23.9509ZM8.94352 22.2426L10.3614 20.3954C10.5131 20.1979 10.748 20.0815 10.9967 20.0815L13.0382 20.0804C13.288 20.0804 13.5229 20.1958 13.6746 20.3944L15.0925 22.2426L16.0588 21.8859L15.9723 19.5327C15.9627 19.2871 16.0662 19.0522 16.2531 18.8932L17.8162 17.5639C18.0073 17.4016 18.2625 17.3375 18.5059 17.3909L20.762 17.8831L21.2841 16.9659L19.7253 15.2181C19.5619 15.0355 19.4914 14.7889 19.5331 14.5476L19.8865 12.5125C19.9292 12.2701 20.0798 12.0598 20.2965 11.9434L22.3465 10.8437L22.1639 9.79625L19.8758 9.47487C19.6302 9.43964 19.4146 9.29336 19.2918 9.07768L18.27 7.28713C18.1483 7.07572 18.1312 6.81947 18.2219 6.59205L19.0985 4.40858L18.3041 3.73379L16.3502 4.97767C16.1399 5.1122 15.8772 5.13996 15.6423 5.05241L13.7279 4.34452C13.4962 4.2591 13.3179 4.07225 13.2421 3.83735L12.53 1.60263H11.5039L10.7928 3.83735C10.717 4.07332 10.5387 4.26017 10.307 4.34558L8.39151 5.05348C8.15662 5.14103 7.89503 5.11327 7.68362 4.97874L5.72864 3.73592L4.93533 4.40858L5.81192 6.59205C5.90268 6.81841 5.88559 7.07466 5.76388 7.28713L4.74314 9.07768C4.62036 9.29336 4.40468 9.43964 4.15911 9.47487L1.86993 9.79732L1.68842 10.8447L3.73843 11.9456C3.95517 12.0619 4.10572 12.2723 4.14843 12.5146L4.50291 14.5486C4.54455 14.7889 4.47408 15.0366 4.31179 15.2192L2.75186 16.9681L3.27397 17.8852L5.53005 17.392C5.77455 17.3386 6.02974 17.4026 6.21979 17.5649L7.78292 18.8932C7.97084 19.0512 8.0744 19.2871 8.06479 19.5327L7.97831 21.887L8.94352 22.2426ZM8.02 12.0011C8.02 9.79519 9.80948 8.00464 12.0164 8.00464C14.2223 8.00464 16.0129 9.79519 16.0129 12.0011C16.0129 14.208 14.2223 15.9975 12.0164 15.9975C9.80948 15.9975 8.02 14.208 8.02 12.0011ZM14.4124 12.0011C14.4124 10.6803 13.3383 9.60619 12.0175 9.60619C10.6957 9.60619 9.62263 10.6803 9.62263 12.0011C9.62263 13.3229 10.6957 14.3959 12.0175 14.3959C13.3383 14.3959 14.4124 13.3229 14.4124 12.0011Z"
                      />
                    </svg>
                  </button>
                  <button
                    v-else
                    @click="mobileNavVisible = false"
                    class="main__btn"
                  >
                    <svg
                      class="main__close-icon"
                      width="14"
                      height="14"
                      viewBox="0 0 14 14"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <path d="M1 1L13 13" stroke-width="2" />
                      <path d="M1 13L13 1.25" stroke-width="2" />
                    </svg>
                  </button>
                  <div
                    class="dropdown dropdown-mobile"
                    :class="{ 'is-active': settingsVisible }"
                  >
                    <div class="dropdown__item dropdown__item_row">
                      <p>Contrast mode</p>
                      <label class="switch">
                        <input
                          @change="changeTheme"
                          class="switch__input"
                          type="checkbox"
                        />
                        <span class="switch__slider"></span>
                      </label>
                    </div>
                    <div class="dropdown__item dropdown__item_row">
                      <p>Analytics</p>
                      <label class="switch">
                        <input class="switch__input" type="checkbox" />
                        <span class="switch__slider"></span>
                      </label>
                    </div>
                    <div class="dropdown__item">
                      <button class="dropdown__item--btn">
                        Koons Silver Spring
                      </button>
                      <button class="dropdown__item--btn">
                        Matt Taylor
                      </button>
                      <button class="dropdown__item--btn is-active">
                        Kenny Ross
                      </button>
                      <button class="dropdown__item--btn">Paul Miller</button>
                      <button class="dropdown__item--btn">Steve Shane</button>
                      <button class="dropdown__item--btn">Bedford</button>
                      <div class="dropdown__item--btns">
                        <button class="dropdown__item--btn">Scraper</button>
                        <button class="dropdown__item--btn">Admin</button>
                        <button class="dropdown__item--btn">History</button>
                        <button class="dropdown__item--btn">Log out</button>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <nav class="main__nav" :class="{ 'is-active': mobileNavVisible }">
              <a href="#" class="main__nav--link main__elem is-active"
                >Real Time Cashflow</a
              ><a href="#" class="main__nav--link main__elem">Planner</a
              ><a href="#" class="main__nav--link main__elem">Budget</a
              ><a href="#" class="main__nav--link main__elem">Lead Sourse ROI</a
              ><a href="#" class="main__nav--link main__elem">Sales</a
              ><a href="#" class="main__nav--link main__elem">Website</a
              ><a href="#" class="main__nav--link main__elem">PPC</a
              ><a href="#" class="main__nav--link main__elem">SEO</a
              ><a href="#" class="main__nav--link main__elem">Fixed OPS</a
              ><a href="#" class="main__nav--link main__elem">Market share</a>
            </nav>
          </div>
          <div class="container">
            <a class="main__logo-mobile" href="/">
              <img src="@/assets/logo.png" alt="ONE VISION" />
            </a>
            <Cashflow />
            <footer class="footer-mobile">
              <p>Questions? Contact us.</p>
              <p>
                © CLC One Vision - Managment solutions, 2020. All right
                reserved.
              </p>
            </footer>
          </div>
        </div>
        <div class="main__btns">
          <button class="main__btn-export main__btn main__elem">PDF</button>
          <button class="main__btn-export main__btn main__elem">XLS</button>
          <button
            @click="settingsVisible = !settingsVisible"
            class="main__btn-settings main__btn main__elem"
          >
            <svg
              class="main__settings-icon"
              width="25"
              height="24"
              viewBox="0 0 25 24"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                fill-rule="evenodd"
                clip-rule="evenodd"
                d="M8.94421 23.9509L6.88139 23.1896C6.55574 23.069 6.3454 22.754 6.35821 22.4081L6.45111 19.8626L5.48696 19.0426L3.04297 19.5765C2.70023 19.6512 2.34896 19.4943 2.17599 19.19L1.07625 17.2617C0.905412 16.9627 0.944917 16.589 1.17341 16.3317L2.85932 14.4419L2.63831 13.1734L0.421738 11.984C0.118508 11.8206 -0.0469871 11.48 0.0117371 11.1405L0.39291 8.94849C0.452702 8.60575 0.726036 8.34096 1.07091 8.29185L3.548 7.94271L4.18222 6.83015L3.23516 4.47051C3.10703 4.15126 3.19779 3.78504 3.46045 3.56188L5.14316 2.13222C5.41009 1.9048 5.79553 1.87811 6.09129 2.06602L8.20963 3.41347L9.38624 2.97891L10.1561 0.558413C10.2628 0.225286 10.5714 0 10.9205 0H13.1179C13.466 0 13.7745 0.225285 13.8813 0.557344L14.6522 2.97785L15.8277 3.41134L17.945 2.06388C18.2408 1.87597 18.6262 1.90266 18.8931 2.13008L20.5769 3.56082C20.8396 3.78397 20.9303 4.14913 20.8022 4.46944L19.8552 6.82908L20.4904 7.94271L22.9665 8.28971C23.3103 8.33883 23.5847 8.60362 23.6445 8.94635L24.0267 11.1384C24.0854 11.4779 23.9199 11.8185 23.6167 11.9819L21.4001 13.1713L21.1802 14.4397L22.865 16.3285C23.0946 16.5848 23.1341 16.9595 22.9643 17.2585L21.8646 19.1878C21.6906 19.4921 21.3393 19.6491 20.9976 19.5744L18.5547 19.0416L17.5895 19.8626L17.6824 22.407C17.6952 22.7529 17.4848 23.0679 17.1603 23.1886L15.0964 23.9509C14.7664 24.0716 14.3959 23.9648 14.1824 23.6861L12.646 21.6831L11.3946 21.6842L9.85711 23.6861C9.64356 23.9648 9.27307 24.0716 8.94421 23.9509ZM8.94352 22.2426L10.3614 20.3954C10.5131 20.1979 10.748 20.0815 10.9967 20.0815L13.0382 20.0804C13.288 20.0804 13.5229 20.1958 13.6746 20.3944L15.0925 22.2426L16.0588 21.8859L15.9723 19.5327C15.9627 19.2871 16.0662 19.0522 16.2531 18.8932L17.8162 17.5639C18.0073 17.4016 18.2625 17.3375 18.5059 17.3909L20.762 17.8831L21.2841 16.9659L19.7253 15.2181C19.5619 15.0355 19.4914 14.7889 19.5331 14.5476L19.8865 12.5125C19.9292 12.2701 20.0798 12.0598 20.2965 11.9434L22.3465 10.8437L22.1639 9.79625L19.8758 9.47487C19.6302 9.43964 19.4146 9.29336 19.2918 9.07768L18.27 7.28713C18.1483 7.07572 18.1312 6.81947 18.2219 6.59205L19.0985 4.40858L18.3041 3.73379L16.3502 4.97767C16.1399 5.1122 15.8772 5.13996 15.6423 5.05241L13.7279 4.34452C13.4962 4.2591 13.3179 4.07225 13.2421 3.83735L12.53 1.60263H11.5039L10.7928 3.83735C10.717 4.07332 10.5387 4.26017 10.307 4.34558L8.39151 5.05348C8.15662 5.14103 7.89503 5.11327 7.68362 4.97874L5.72864 3.73592L4.93533 4.40858L5.81192 6.59205C5.90268 6.81841 5.88559 7.07466 5.76388 7.28713L4.74314 9.07768C4.62036 9.29336 4.40468 9.43964 4.15911 9.47487L1.86993 9.79732L1.68842 10.8447L3.73843 11.9456C3.95517 12.0619 4.10572 12.2723 4.14843 12.5146L4.50291 14.5486C4.54455 14.7889 4.47408 15.0366 4.31179 15.2192L2.75186 16.9681L3.27397 17.8852L5.53005 17.392C5.77455 17.3386 6.02974 17.4026 6.21979 17.5649L7.78292 18.8932C7.97084 19.0512 8.0744 19.2871 8.06479 19.5327L7.97831 21.887L8.94352 22.2426ZM8.02 12.0011C8.02 9.79519 9.80948 8.00464 12.0164 8.00464C14.2223 8.00464 16.0129 9.79519 16.0129 12.0011C16.0129 14.208 14.2223 15.9975 12.0164 15.9975C9.80948 15.9975 8.02 14.208 8.02 12.0011ZM14.4124 12.0011C14.4124 10.6803 13.3383 9.60619 12.0175 9.60619C10.6957 9.60619 9.62263 10.6803 9.62263 12.0011C9.62263 13.3229 10.6957 14.3959 12.0175 14.3959C13.3383 14.3959 14.4124 13.3229 14.4124 12.0011Z"
              />
            </svg>
          </button>
          <div class="dropdown" :class="{ 'is-active': settingsVisible }">
            <div class="dropdown__item dropdown__item_row">
              <p>Contrast mode</p>
              <label class="switch">
                <input
                  @change="changeTheme"
                  class="switch__input"
                  type="checkbox"
                />
                <span class="switch__slider"></span>
              </label>
            </div>
            <div class="dropdown__item dropdown__item_row">
              <p>Analytics</p>
              <label class="switch">
                <input class="switch__input" type="checkbox" />
                <span class="switch__slider"></span>
              </label>
            </div>
            <div class="dropdown__item">
              <button class="dropdown__item--btn">Koons Silver Spring</button>
              <button class="dropdown__item--btn">
                Matt Taylor
              </button>
              <button class="dropdown__item--btn is-active">
                Kenny Ross
              </button>
              <button class="dropdown__item--btn">Paul Miller</button>
              <button class="dropdown__item--btn">Steve Shane</button>
              <button class="dropdown__item--btn">Bedford</button>
              <div class="dropdown__item--btns">
                <button class="dropdown__item--btn">Scraper</button>
                <button class="dropdown__item--btn">Admin</button>
                <button class="dropdown__item--btn">History</button>
                <button class="dropdown__item--btn">Log out</button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </main>
    <footer class="footer">
      <p>Questions? Contact us.</p>
      <p>© CLC One Vision - Managment solutions, 2020. All right reserved.</p>
    </footer>
  </div>
</template>

<script>
import Cashflow from "@/views/Cashflow.vue";

export default {
  name: "App",
  components: {
    Cashflow,
  },
  data() {
    return {
      mobileNavVisible: false,
      settingsVisible: false,
    };
  },
  methods: {
    changeTheme({ target }) {
      const html = document.documentElement;
      if (target.checked) {
        localStorage.setItem("theme", "dark");
        html.dataset.theme = "dark";
      } else {
        localStorage.setItem("theme", "light");
        html.dataset.theme = "light";
      }
    },
  },
};
</script>

<style lang="scss">
:root {
  --color1: #3e4756;
  --color2: rgba(0, 0, 0, 0.08);
  --color3: #f8f8f8;
  --color4: rgba(62, 71, 86, 0.12);
  --color5: #ebebeb;
  --color6: #fff;
  --color7: #dadcde;
  --color8: #f8f8f8;
  --color9: #dadcde;
}

[data-theme="dark"] {
  --color1: #fff;
  --color2: rgba(255, 255, 255, 0.15);
  --color3: #3f4042;
  --color4: rgba(255, 255, 255, 0.08);
  --color5: rgba(255, 255, 255, 0.16);
  --color6: #2e2f32;
  --color7: #5e5f60;
  --color8: #2e2f32;
  --color9: rgba(255, 255, 255, 0.4);
}

.pos {
  &-relative {
    position: relative;
  }
}

body {
  background: var(--color6);
  margin: 0;
  padding: 0;
}

body,
button,
select {
  font: 400 16px "Helvetica Neue", sans-serif;
  color: var(--color1);
}

* {
  box-sizing: border-box;
}

h1,
h2,
h3,
h4,
h5,
h6 {
  font-weight: 400;
  letter-spacing: 0.02em;
  margin: 0;
}

h2 {
  font-size: 24px;
}

p {
  margin: 0;
}

a {
  color: var(--color1);
  text-decoration: none;
}

button {
  background: transparent;
  display: block;
  border: none;
  outline: none;
  cursor: pointer;
  padding: 0;
}

select {
  background: transparent;
  outline: none;
  border: none;
  appearance: none;
}

.container {
  width: 100%;
  max-width: 1262px;
  padding: 0 0 0 78px;
  margin: 0 auto;
}

.dropdown {
  visibility: hidden;
  opacity: 0;
  background: var(--color3);
  width: 252px;
  position: absolute;
  top: 104px;
  right: 28px;
  border-radius: 12px;
  z-index: 9;
  transition: all 0.2s;
  &.is-active {
    visibility: visible;
    opacity: 1;
  }
  &-mobile {
    display: none;
  }
  &::before {
    bottom: 100%;
    right: 23px;
    border: 9px solid transparent;
    content: " ";
    height: 0;
    width: 0;
    position: absolute;
    border-bottom-color: var(--color3);
  }
  &__item {
    padding: 16px;
    &:not(:last-child) {
      border-bottom: 1px solid var(--color6);
    }
    &_row {
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
    &--btns {
      margin-top: 20px;
    }
    &--btn {
      font-size: inherit;
      margin-bottom: 5px;
      &.is-active {
        &::after {
          content: url(./assets/checked.svg);
          margin-left: 2px;
        }
      }
    }
  }
  &-arrow {
    width: 24px;
    height: 24px;
    display: flex;
    align-items: center;
    justify-content: center;
    background: var(--color8);
    border-radius: 12px;
    margin-left: 9px;
    svg {
      fill: var(--color1);
    }
  }
}

.switch {
  position: relative;
  display: inline-block;
  width: 64px;
  height: 32px;
  &__input {
    opacity: 0;
    width: 0;
    height: 0;
    &:checked + .switch__slider {
      border-color: #f38c2c;
      &::before {
        background: #f38c2c;
        transform: translateX(-29px);
      }
    }
  }
  &__slider {
    position: absolute;
    cursor: pointer;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: transparent;
    border: 2px solid #ebebeb;
    border-radius: 32px;
    transition: 0.2s;
    &::before {
      position: absolute;
      content: "";
      height: 20px;
      width: 20px;
      right: 5px;
      bottom: 4px;
      border-radius: 50%;
      background: #ebebeb;
      transition: 0.2s;
    }
  }
}

.main {
  padding: 18px 20px;
  &__btn {
    width: 64px;
    height: 48px;
    &-export {
      background: transparent;
      border: 1px solid var(--color5);
      margin-right: 8px;
      &:hover,
      &.is-active {
        border: 1px solid #3cbf73;
      }
    }
    &-settings {
      display: flex;
      align-items: center;
      justify-content: center;
      margin-left: 48px;
      &:hover,
      &.is-active {
        border: 1px solid #f38c2c;
      }
    }
  }
  &__row {
    display: flex;
    justify-content: space-between;
    &-mobile {
      &--inner {
        display: flex;
      }
      &--settings {
        display: none;
      }
    }
  }
  &__elem {
    background: var(--color3);
    letter-spacing: 0.02em;
    border-radius: 12px;
  }
  &__nav {
    display: flex;
    flex-wrap: wrap;
    padding: 0 78px;
    margin: 0 -4px;
    &-dropdown {
      display: none;
    }
    &--link {
      letter-spacing: 0.02em;
      display: block;
      padding: 15px;
      margin: 0 4px 8px;
      &.is-active {
        background: var(--color1);
        color: var(--color6);
      }
    }
  }
  &__btns {
    display: flex;
  }
  &__settings-icon {
    fill: var(--color1);
  }
  &__close-icon {
    stroke: var(--color1);
  }
  &__logo-mobile {
    display: none;
  }
}

.footer {
  font-size: 12px;
  display: flex;
  justify-content: space-between;
  padding: 0 20px 21px;
  margin-top: 181px;
  &-mobile {
    display: none;
  }
}

@media screen and (max-width: 1024px) {
  body,
  button,
  select {
    font-size: 14px;
  }
  h2 {
    font-size: 18px;
  }
  .container {
    max-width: 496px;
    padding: 0 16px;
  }
  .dropdown {
    top: 68px;
    right: -9px;
    display: none;
    &-mobile {
      display: block;
    }
    &__btn {
      font-size: 14px;
    }
    &-arrow {
      width: 20px;
      height: 20px;
      &.is-active {
        background: #f38c2c;
        svg {
          color: #fff;
        }
      }
      svg {
        width: 9.43px;
        height: 5.89px;
      }
    }
  }
  .main {
    padding: 0 0 19px;
    &__row {
      display: block;
      &-mobile {
        background: var(--color3);
        &--inner {
          display: flex;
          justify-content: space-between;
          align-items: center;
          height: 40px;
        }
        &--settings {
          display: block;
        }
      }
    }
    &__nav {
      display: none;
      flex-direction: column;
      border-top: 1px solid var(--color5);
      padding: 10px 0 0;
      margin: 0;
      &.is-active {
        display: block;
      }
      &--link {
        background: transparent;
        border-radius: 0;
        padding-top: 10px;
        padding-bottom: 10px;
        margin: 0;
        &.is-active {
          color: var(--color9);
          background: transparent;
        }
      }
      &-dropdown {
        width: 100%;
        display: flex;
        justify-content: space-between;
        align-items: center;
      }
    }
    &__logo {
      display: none;
      &-mobile {
        display: inline-block;
        margin-top: 28px;
        img {
          width: 128px;
          height: 27.86px;
        }
      }
    }
    &__btns {
      display: none;
    }
    &__btn {
      background: transparent;
      width: auto;
      height: auto;
      margin: 0 14px 0 51px;
      position: relative;
      &::before {
        content: "";
        width: 1px;
        height: 24px;
        background: var(--color5);
        position: absolute;
        top: 50%;
        left: -29px;
        transform: translateY(-50%);
      }
      svg {
        width: 16.15px;
        height: 16.12px;
      }
    }
  }
  .footer {
    display: none;
    &-mobile {
      display: block;
      width: 220px;
      font-size: 10px;
      line-height: 1.6;
      margin: 65px 0 0;
    }
  }
}
</style>
