<template>
  <div class="container">
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
    <main>
    <!--   home   -->
      <div id= "home" class= "big-bg"><!--大きな画像-->
          <div class= "home-content">
              <h2 class= "page-title">信州珈琲</h2>
              <h3 class= "page-subtitle">自家焙煎コーヒー工房</h3>
          </div>
      </div>
        <div id = "main-2column" class = "main-container">
          <div class = "item1">
              <div class = "sub-container">
                  <div class = "item">
                      <p>自家焙煎コーヒー工房 信州珈琲について</p>
                      <p>長野県上田市にある小さな珈琲工房です。注文を受けてから焙煎しているので、毎朝焼きたてのコーヒー豆をお届けしています。コーヒーは産地や焼き加減で様々な味わいを楽しむことができます。甘味、酸味、コクのあるあなただけのコーヒーを見つけるお手伝いをしています。</p>
                      <img src= "../assets/images/7a9552317fc03676cb88252c7702ba01_4640324325e0face43a278ac96b1f045.jpeg" alt= "コーヒー豆の画像、ショップの紹介"></div>
                  
                  <div class = "item">
                      <p>信州珈琲では自然豊かな長野県（信州）をテーマにした6種類のブレンドをご用意しています。</p>
                      <img src= "../assets/images/2fda7af08a7a0065d62bf339a9256ba6_6c12f280e6b36b744334636a210331ec.jpeg" alt= "6種類のブレンドの紹介画像"></div>
                  <div class = "item"><img src= "../assets/images/eed0c7d4705017ec302341bc93c97551_f2a82b44835efaccba9d50db059f2bb9.jpeg" alt= "信濃路ブレンド"></div>
                  <div class = "item"><img src= "../assets/images/b5ec43b9801f89acb20a01047570652b_ef2a8c4956508da9db460614edb0c683.jpeg" alt= "軽井沢ブレンド"></div>
                  <div class = "item"><img src= "../assets/images/ccd00ee34702b93c24b92933d03ff248_9dd6589e55a2464351b54ec9d98730c1.jpeg" alt= "上高地ブレンド"></div>
                  <div class = "item"><img src= "../assets/images/9bb5114a1ce4fa6fc5a5d8a75303c596_c13a68b90555d38e7f70544aeb71b8b8.jpeg" alt= "白樺ブレンド"></div>
                  <div class = "item"><img src= "../assets/images/bfba1e78ed29df1e5ef950046759aa3d_9a1f72115995f5f69633b9e9005a9af9.jpeg" alt= "浅間ブレンド"></div>
                  <div class = "item"><img src= "../assets/images/033c0e0d14bac311e05bcf0c29b27caf_148acf5a38e27ad970ec0d73b1795b8c.jpeg" alt= "そよ風ブレンド"></div>
                  <div class = "item">9</div>
              </div>

          </div>
          <!-- サイドボード非表示 <div id= "mainw" class = "item main-weapper">サイドボード
          </div>-->
        </div>
    </main>
    <footer class="footer">
      <div>
        フッターエリア
      </div>
    </footer>
  </div>
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

<!-- Add "scoped" attribute to limit CSS to this component only -->
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
