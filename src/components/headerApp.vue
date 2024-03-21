<template>
    <!--<div class="container">-->
      <header class="header">
        <div class="header__inner">
          <h1 class="header__title header-title">
              SHINSHUCOFFEE
          </h1>
  
    <div>
      <!-- ここにコンポーネントのHTMLを追加 -->
      <nav class="header__nav nav" id="js-nav">
            <ul class="nav__items nav-items">
              <li class="nav-items__item"><a href="">ホーム</a></li>
              <li class="nav-items__item"><a href="">オンラインショップ</a></li>
              <li class="nav-items__item"><a href="">ログイン</a></li>
              <li class="nav-items__item"><a href="">お問い合わせ</a></li>
            </ul>
          </nav>
  
      <!-- ハンバーガーボタン -->
      <div id="js-hamburger" @click="toggleMenu" :class="{ active: isHamburgerActive }">
        <!-- ここにハンバーガーボタンの内容を追加 -->
      </div>
  
      <!-- ナビゲーションメニュー -->
      <div id="js-nav" :class="{ active: isNavActive }">
        <!-- ここにナビゲーションメニューの内容を追加 -->
      </div>
    </div>
            <button class="header__hamburger hamburger" id="js-hamburger">
            <span></span>
            <span></span>
            <span></span>
          </button>
        </div>
      </header>
</template>

<script>

export default {
  data() {
    return {
      isHamburgerActive: false,
      isNavActive: false
    };
  },
  methods: {
    toggleMenu() {
      this.isHamburgerActive = !this.isHamburgerActive;
      this.isNavActive = !this.isNavActive;
    }
  }
};


</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
img {
  max-width: 100%;
}
html {
  font-size: 100%;
}
body {
  font-family: "Yu Gothic Medium" , "游ゴシック Medium" , YuGothic , "游ゴシック体", "ヒラギノ角ゴ Pro W3" , sans-serif;
  line-height: 1.7;
      color: #432;
}


a {
  text-decoration: none;
}

ul,
li {
  list-style: none;
}



.footer {
  background-color: #f6f6f6;
  height: 200px;
  display: flex;
}

.footer div {
  margin: auto;
}


/* ヘッダー */


.header {
  background-color: white;
  width: 100%;
  height: 50px;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 999;
}

.header__inner {
  padding: 0 20px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: inherit;
  position: relative;
}


/* ヘッダーのロゴ部分 */
.header__title {
  width: 80px;
}


@media screen and (min-width: 960px) {
  .header__title {
    width: 120px;
  }
}

.header__title img {
  display: block;
  width: 100%;
  height: 100%;
}

/* ヘッダーのナビ部分 */

.header__nav {
  position: absolute;
  right: 0;
  left: 0;
  top: 0;
  width: 100%;
  height: 100vh;
  transform: translateX(100%);
  background-color: #fff;
  transition: ease .4s;
}


@media screen and (min-width: 960px) {
  .header__nav {
    position: static;
    transform: initial;
    background-color: inherit;
    height: inherit;
    display: flex;
    justify-content: end;
    width: 50%;
  }
}


@media screen and (min-width: 960px) {
  .nav__items {
    width: 100%;
    display: flex;
    align-items: center;
    height: initial;
    justify-content: space-between;
  }
  .nav-items__item a {
    font-size: 0.4rem;
  }
}

.nav-items {
  padding-top: 250px;
  padding-bottom: 200px;
}


@media screen and (min-width: 960px) {
  .nav-items {
    padding-top: inherit;
    padding-bottom: inherit;
  }
}

/* ナビのリンク */
.nav-items__item a {
  color: black;
  width: 100%;
  display: block;
  text-align: center;
  font-size: 15px;
  margin-bottom: 24px;
}

.nav-items__item:last-child a {
  margin-bottom: 0;
}

@media screen and (min-width: 960px) {
  .nav-items__item a {
    margin-bottom: 0;
  }
}


/* ハンバーガーメニュー */

.header__hamburger {
  width: 48px;
  height: 100%;

}

.hamburger {
  background-color: transparent;
  border-color: transparent;
  z-index: 9999;
}

@media screen and (min-width: 960px) {
  .hamburger {
    display: none;
  }
}

/* ハンバーガーメニューの線 */
.hamburger span {
  width: 100%;
  height: 1px;
  background-color: #000;
  position: relative;
  transition: ease .4s;
  display: block;
}

.hamburger span:nth-child(1) {
  top: 0;
}

.hamburger span:nth-child(2) {
  margin: 8px 0;
}

.hamburger span:nth-child(3) {
  top: 0;
}


/* ハンバーガーメニュークリック後のスタイル */
.header__nav.active {
  transform: translateX(0);
}

.hamburger.active span:nth-child(1) {
  top: 5px;
  transform: rotate(45deg);
}

.hamburger.active span:nth-child(2) {
  opacity: 0;

}

.hamburger.active span:nth-child(3) {
  top: -13px;
  transform: rotate(-45deg);
}


/*------------------------------- */
/*home*/
.home-content {
  text-align: center;
  vertical-align: middle;
  margin-top: 40px;
  font-family: 'Philosopher' , serif;
  background-color: black;
}
/* 大きな画像*/
.big-bg {
  background-size: cover;
  background-position: center top;
  
}

h2,h3 {
  vertical-align: middle;
}
.page-title {
  font-size: 2.5rem;
  font-family: 'Philosopher' , serif;
  text-transform: uppercase;
  font-weight: normal;
  color: #ffffffff;
  text-shadow: 2px 2px 3px #432;
  margin-top: 10px;
}
.page-subtitle {
  font-size: 2rem;
  font-family: 'Philosopher' , serif;
  text-transform: uppercase;
  font-weight: normal;
  color: #ffffffff;
  text-shadow: 2px 2px 3px #432;
  margin-top: 10px;
}
p {
  font-family: 'Philosopher' , serif;
  padding: 45px;
  margin-bottom: 10px;
  max-width: 600px;
  font-size: 1rem;
}
.item {
  color: #432;
  text-align: justify;
  padding: 10px;
  max-width: 800px;
  margin-top: 10px;
}
.item1 {
  margin-left: 20px;
}

.sub-container {
  display: flex;
  flex-direction: column;
}

article,
aside {
  width: 100%;
}

#mainw {
  background: brown;
  color: floralwhite;
  padding: 10px;
  margin-left: 20px;
}

/* main-content */
@media(max-width: 600px){
  .main-container{
    display: flex;
    flex-direction: column;
  }
}

/*  レスポンシブPC
-----------------------------------*/
@media(min-width: 960px) {
  
  .page-title {
    font-size: 5rem;
  }
  .page-subtitle {
    font-size: 3.5rem;
  }
}
.main-container {
    display: flex;
    justify-content: space-around;
}

</style>

  