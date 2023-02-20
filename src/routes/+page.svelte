<script>
import Arrow from '../components/Arrow.svelte';
import Footer from '../components/Footer.svelte';
import { onMount, beforeUpdate } from 'svelte';
import gsap from 'gsap';
import { browser } from '$app/environment';
import { Swiper, SwiperSlide } from "swiper/svelte";
import "swiper/css";
import { Scrollbar } from "swiper";
import 'swiper/css/scrollbar';

onMount(() => {

  if (browser) {
    let idxtp = document.getElementById('in-fr');
    idxtp.style.visibility = "visible";
  }
  
  const tl = gsap.timeline();
  tl.from('#index-top .wrapper #top-Visual img', {
    duration: .1,
    x: "-10.5vw",
    ease: 'power3.inOut',
  })   
  
});

</script>

<svelte:head>
	<title>日々に豊かさを添える焼酎 | SHOCHU.X 焼酎屋 </title>
  <script src="https://webfont.fontplus.jp/accessor/script/fontplus.js?kqbwQX--jVA%3D&box=bYUqUdOYlP4%3D&aa=1&ab=2"></script>
</svelte:head>


<main> 

<section id="in-top">
  <div class="wrapper">

    <div class="visual">
      <img src="../image/about.jpg" alt="">
    </div>
    <div class="tagline">
      <h1 class="h2">暮らしに豊かさを添える焼酎</h1>
      <p class="h5">わたしたちは、日本の蒸溜酒である焼酎を大切に、<br>
        そして、その魅力を形にし、お届けいたします。<br>
        ゆったりお愉しみいただける焼酎をご堪能ください。
      </p>
      <a href="/about" class="h6 l-link">わたしたち焼酎屋について</a>
    </div>

  </div>
</section>

<section id="in-news" class="pc-side">
  <div class="l-section-head">
    <h2 class="h1">商品やイベントに<br>関するお知らせ</h2>
    <h3 lang="en">Information</h3>
    <p class="pc">
      わたしたちの商品は、より多くの方にお手に取って<br>
      いただけるよう販路の拡大とともに、焼酎の魅力を<br>
      お伝えするイベントやセミナーを開催しております。
    </p>
  </div>
  
  <div class="wrapper">
    <a href="/" class="l-word container">
        <div class="left">
            <div class="l-line"></div> 
            <div class="h6 date" lang="en">8th October 2022</div> 
            <h2 class="h5 sans">東急渋谷フードショーにて、テイスティングセミナーを行いました</h2>
        </div> 
        <div class="right">
            <Arrow />
        </div>
    </a>
    <a href="/" class="l-word container">
        <div class="left">
            <div class="l-line"></div> 
            <div class="h6 date" lang="en">8th October 2022</div> 
            <h2 class="h5 sans">フレンチオークリザーブド（NK麦759）を10/17 (月) 21時から販売開始しました。</h2>
        </div> 
        <div class="right">
            <Arrow />
        </div>
    </a>
    <a href="/" class="l-word container">
        <div class="left">
            <div class="l-line"></div> 
            <div class="h6 date" lang="en">8th October 2022</div> 
            <h2 class="h5 sans">東急渋谷フードショーにて、テイスティングセミナーを行いました</h2>
        </div> 
        <div class="right">
            <Arrow />
        </div>
    </a>
    <div class="l-line"></div> 
    <a href="/" class="h6 l-link">すべての記事をみる</a>
</div>
</section>

<section id="in-product">
  <div class="wrapper">

    <a href="/" class="container">
      <img src="../image/product.jpeg" alt="">
      <h2 class="h2">全麹三段仕込みの麦焼酎「希継奈」</h2>
      <p class="h5 half">『全麹三段仕込み』製法により、甘みとコクが存分に引き出された原酒を5年間熟成することで、</p>
      <div class="bottom">
        <div class="h3 price" lang="en">¥6,800</div>
        <div class="h4 l-buy">購入する</div>
      </div>
    </a>
    <a href="/" class="container">
      <img src="../image/product.jpeg" alt="">
      <h2 class="h2">全麹三段仕込みの麦焼酎「希継奈」</h2>
      <p class="h5 half">『全麹三段仕込み』製法により、甘みとコクが存分に引き出された原酒を5年間熟成することで、</p>
      <div class="bottom">
        <div class="h3 price" lang="en">¥6,800</div>
        <div class="h4 l-buy">購入する</div>
      </div>
    </a>
    <a href="/" class="container">
      <img src="../image/product.jpeg" alt="">
      <h2 class="h2">全麹三段仕込みの麦焼酎「希継奈」</h2>
      <p class="h5 half">『全麹三段仕込み』製法により、甘みとコクが存分に引き出された原酒を5年間熟成することで、</p>
      <div class="bottom">
        <div class="h3 price" lang="en">¥6,800</div>
        <div class="h4 l-buy">購入する</div>
      </div>
    </a>
  </div>

  <div class="carousel pc-side">
    <div class="l-section-head">
      <h2 class="h1">商品やイベントに<br>関するお知らせ</h2>
      <h3 lang="en">Information</h3>
      <p class="pc">
        わたしたちの商品は、より多くの方にお手に取って<br>
        いただけるよう販路の拡大とともに、焼酎の魅力を<br>
        お伝えするイベントやセミナーを開催しております。
      </p>
    </div>
    <Swiper
      modules={[Scrollbar]}
      speed={1000}
      slidesPerView={"auto"}
      spaceBetween={10}
      scrollbar={{ draggable: true }}
      class="mySwiper wrapper"
    >
    <SwiperSlide>
    <a href="/" class="container">
      <img src="../image/product.jpeg" alt="">
      <h2 class="h2">檸檬と希継奈</h2>
      <p class="h5 half">糸島産無農薬檸檬を使った麦焼酎『希継奈』のカクテルをボトリングいたしました。</p>
      <div class="bottom">
        <div class="h4 price" lang="en">¥6,800</div>
        <div class="h5 l-buy">購入する</div>
      </div>
    </a>
    </SwiperSlide>
    <SwiperSlide>
    <a href="/" class="container">
      <img src="../image/product.jpeg" alt="">
      <h2 class="h2">檸檬と希継奈</h2>
      <p class="h5 half">糸島産無農薬檸檬を使った麦焼酎『希継奈』のカクテルをボトリングいたしました。</p>
      <div class="bottom">
        <div class="h4 price" lang="en">¥6,800</div>
        <div class="h5 l-buy">購入する</div>
      </div>
    </a>
    </SwiperSlide>
    <SwiperSlide>
    <a href="/" class="container">
      <img src="../image/product.jpeg" alt="">
      <h2 class="h2">檸檬と希継奈</h2>
      <p class="h5 half">糸島産無農薬檸檬を使った麦焼酎『希継奈』のカクテルをボトリングいたしました。</p>
      <div class="bottom">
        <div class="h4 price" lang="en">¥6,800</div>
        <div class="h5 l-buy">購入する</div>
      </div>
    </a>
    </SwiperSlide>
    </Swiper>
    
  </div>
</section>


<section id="in-cocktail">
  <div class="l-section-head">
    <img src="../image/cocktail.jpeg" alt="">
    <h2 class="h2">焼酎カクテルを愉しむ</h2>
    <p class="h5">焼酎は、さまざまなバーでみかけるお酒ー蒸溜酒の<br>
      一つであり、ストレートで頂く以外にもたくさんの<br>
      愉しみ方があります。私たちの蒸溜酒は、アルコール<br>
      度数も高く、さまざまなシーンでお愉しみいただけます。</p>
  </div>
  <div class="wrapper l-cards">
    
    <a href="/" class="l-card">
      <img src="../image/cocktail_2.jpeg" alt="">
      <h3 class="h3">焼酎香るレモンサワー</h3>
      <div class="h6 half" lang="en">Lemon Sour</div>
      <p class="h5 opacity">焼酎の力づよい香りに、爽やかな檸檬がキレを表現し、<br>
        食卓をフレッシュに彩るロングカクテルです。
      </p>
      <a href="/" class="l-link">記事を詳しく</a>
    </a>

    <a href="/" class="l-card">
      <img src="../image/cocktail_2.jpeg" alt="">
      <h3 class="h3">焼酎香るレモンサワー</h3>
      <div class="h6 half" lang="en">Lemon Sour</div>
      <p class="h5 opacity">焼酎の力づよい香りに、爽やかな檸檬がキレを表現し、<br>
        食卓をフレッシュに彩るロングカクテルです。
      </p>
      <a href="/" class="l-link">記事を詳しく</a>
    </a>
  </div>
</section>

<section id="in-shop">
  <img src="../image/about.jpg" alt="">
  <div class="section-head">
    <h2 class="h2">取り扱い店舗のご紹介</h2>
    <div class="h5 half" lang="en">Introduce our partners</div>
    <p>
      焼酎カルチャー発信地の九州は勿論のこと、東京や大阪、
      そのほか多くの地域にてお取り扱いいただいています。
      ぜひお近くのレストラン・バーでお愉しみください。
    </p>
  </div>
  <div class="container">
    <a href="/">
      <h3 class="h3" lang="en">Mixlogy Boutique</h3>
      <div class="h5" lang="en">Bar / Tokyo</div>
    </a>
    <a href="/">
      <h3 class="h3" lang="en">Folklore</h3>
      <div class="h5" lang="en">Bar / Tokyo</div>
    </a>
    <a href="/">
      <h3 class="h3" lang="en">Yellow Nakameguro</h3>
      <div class="h5" lang="en">Bar / Tokyo</div>
    </a>
    <a href="/">
      <h3 class="h3" lang="en">Tsugumi</h3>
      <div class="h5" lang="en">Restaurant / Tokyo</div>
    </a>
    <a href="/">
      <h3 class="h3" lang="en">Ritz Carlton</h3>
      <div class="h5" lang="en">Bar / Tokyo</div>
    </a>
  </div>
  <a href="/" class="l-link">ほかの店舗も確認する</a>
</section>


<section id="in-link">
  <div class="wrapper">
    <a href="/" class="container">
      <h2 class="h1">想いを形にー。</h2>
      <p>
        わたしたちが描く焼酎の姿に想いを寄せ、<br>
        形にするべくお力添えいただいている酒造のみなさま。
      </p>
    </a>
    <a href="/" class="container">
      <h2 class="h1">想いを形にー。</h2>
      <p>
        わたしたちが描く焼酎の姿に想いを寄せ、<br>
        形にするべくお力添えいただいている酒造のみなさま。
      </p>
    </a>
  </div>
</section>


<section id="in-archive">
  <div class="section-head">
    <img src="../image/cocktail.jpeg" alt="">
    <h2 class="h2">オフラインイベント</h2>
    <p class="h5">
      わたしたちは、焼酎の魅力や愉しみ方を共有する場として、<br>
      さまざまなバーや百貨店、コミュニティにてセミナーや<br>
      ワークショップを開催しております。アーカイブを<br>
      まとめてありますので、ぜひご覧ください。</p>
  </div>
  <div class="wrapper l-cards">
    
    <a href="/" class="l-card">
      <img src="../image/cocktail_2.jpeg" alt="">
      <h3 class="h3">湯割りと燗酎</h3>
      <div class="h6 half" lang="en">at Nihonbashi SOIL</div>
      <p class="h5 opacity">焼酎の力づよい香りに、爽やかな檸檬がキレを表現し、<br>
        食卓をフレッシュに彩るロングカクテルです。
      </p>
      <a href="/" class="l-link">記事を詳しく</a>
    </a>

    <a href="/" class="l-card">
      <img src="../image/cocktail_2.jpeg" alt="">
      <h3 class="h3">湯割りと燗酎</h3>
      <div class="h6 half" lang="en">at Nihonbashi SOIL</div>
      <p class="h5 opacity">焼酎の力づよい香りに、爽やかな檸檬がキレを表現し、<br>
        食卓をフレッシュに彩るロングカクテルです。
      </p>
      <a href="/" class="l-link">記事を詳しく</a>
    </a>
  </div>
</section>

<section id="in-mail">
  <img src="../image/about.jpg" alt="">
  <img src="../image/product.jpeg" alt="">
  <div class="section-head">
    <h2 class="h2">ニュースレター</h2>
    <p class="h5">
      焼酎の魅力やその奥深さ、また限定イベントのお知らせを
      ニュースレターを通して、告知させていただく場合もございます。
    </p>
  </div>
  <form action="">
    <input class="h4" type="email" name="contact[email]" aria-label="メールアドレス" placeholder="メールアドレス">
    <button class="h4">登録</button>
  </form>
</section>

</main>


<style>
  /*#index-top .wrapper, #index-top .main {opacity: 0;}*/
  #in-fr {visibility: hidden;}
  @keyframes -global-scroll-animation {
    0% {transform: translateY(1rem);opacity: 0;}
    100% {transform: translateY(0);opacity: 1;}
  }

  #in-top {
    position: relative;
    height: 100vh;
    height: 100dvh;
  }
  #in-top .wrapper {
    position: absolute;
    bottom: 5.5rem;
  }
  #in-top .wrapper .visual {
    width: calc(100vw - var(--padding));
    height: calc(100vh - (10rem + 5.5rem + 4rem + 2rem + (1.5rem * 1.8 + 3.6rem * 1.9 + 1.0rem * 1.8)));
    height: calc(100dvh - (10rem + 5.5rem + 4rem + 2rem + (1.5rem * 1.8 + 3.6rem * 1.9 + 1.0rem * 1.8)));
    height: calc(100vh - (4rem + 2rem + (1.5rem * 1.8 + 3.6rem * 1.9 + 1.0rem * 1.8)));
    height: calc(100dvh - (4rem + 2rem + (1.5rem * 1.8 + 3.6rem * 1.9 + 1.0rem * 1.8)));
    margin-bottom: 4rem;
  }
  #in-top .wrapper .visual img {height: 100%;}
  #in-top .wrapper .tagline p {
    font-size: 1.1rem;
    margin: .8rem 0 1.2rem;
    margin-left: .5px;
    opacity: .75;
  }
  #in-top .wrapper .tagline a {margin-left: 1.4px;}
  


  #in-news {margin-top: 4rem;}
  #in-news .wrapper {margin-top: 3rem;}
  #in-news .l-link {margin-top: 3.5rem;}




  #in-product {margin-top: 10rem;}
  #in-product .container {
    width: 100%;
    margin-bottom: 5rem;
  }

  #in-product .container img {
    width: 100%;
    height: calc((100% - var(--padding)*2)/3*2);
  }
  #in-product .container h2 {margin: 1.5rem 0 0.5rem;}
  #in-product .container p {width: 85%;}
  #in-product .container .bottom {
    width: 100%;
    display: flex;
    justify-content: space-between;
    margin-top: 2rem;
  }
  
  #in-product .carousel {
    width: 100vw;
    margin-left: calc(-1 * var(--padding));
    margin-top: 3rem;
  }
  #in-product .carousel h1 {
    margin-left: var(--padding);
    margin-bottom: 2rem;
  }

  #in-product .carousel .container {width: 100%;}
  #in-product .carousel .container p {width: 92.5%;}
  #in-product .carousel .container .bottom {
    margin-top: 1.5rem;
    padding-right: .5rem;
  }

  #in-cocktail {margin-top: 10rem;}

  #in-shop {
    margin-top: 8rem;
    background-color: #E7E6E5;
    padding-bottom: 6rem;
  }
  #in-shop img {
    margin-top: -4rem;
    margin-left: calc(-1 * var(--padding));
  }
  #in-shop .container {
    display: flex;
    justify-content: flex-start;
    align-items: flex-start;
    flex-wrap: wrap;
    margin-top: 5rem;
    margin-bottom: 3rem;
  }
  #in-shop .container a {
    display: block;
    width: 50%;
    margin-bottom: 2.5rem;
  }
  #in-shop .container a div {
    opacity: .5;
    margin-top: .25rem;
  }

  #in-link {margin: 10rem 0 6rem;}
  #in-link .container {margin-bottom: 4rem;}


  #in-mail {
    margin-top: 8rem;
    background-color: #E7E6E5;
    padding-bottom: 6rem;
    position: relative;
  }
  #in-mail img:nth-of-type(1) {
    margin-top: -4rem;
    margin-left: calc(-1 * var(--padding));
  }
  #in-mail img:nth-of-type(2) {
    width: calc(100% - 3 * var(--padding));
    margin-left: calc(4 * var(--padding));
    margin-top: -30vw;
  }

  #in-mail form {
    width: 90%;
    border-bottom: solid .5px var(--textColor);
    display: flex;
    justify-content: space-between;
    padding: 0 0.25rem 0.75rem 0.1rem;
  }



@media screen and (min-width: 720px) {

  #in-top .wrapper {
    position: relative;
    bottom: auto;
  }
  #in-top .wrapper .visual {
    width: 100vw;
    height: 100vh;
    height: 100dvh;
    margin-left: calc(-1 * var(--pcPadding));
  }

  #in-top .wrapper .tagline {
    position: absolute;
    z-index: 1;
    bottom: 8rem;
    top: auto;
  }


  #in-news {margin-top: 16rem;}
  #in-news .wrapper {overflow: hidden;}

  #in-product {margin-top: 14.5rem;}
  #in-product .wrapper {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    column-gap: calc(.5 * var(--pcPadding));
  }
  #in-product .wrapper .container img {
    height: calc((100vw - var(--pcPadding) * 3) / 3 / 16 * 9);
  }


  #in-product .carousel {
    margin-top: 10rem;
    padding-top: 15rem;
    padding-bottom: 12rem;
    margin-left: calc(-1 * var(--pcPadding));
    padding-left: var(--pcPadding);
    background-color: var(--footerColor);
  }
  #in-product .carousel .container {width: 18.5vw;}
  #in-product .carousel .container h2 {font-size: 1.3rem;}
  #in-product .carousel .container h3, 
  #in-product .carousel .container .l-buy {display: none;}



  #in-cocktail {margin-top: 0;}
  #in-cocktail .wrapper {
    display: grid;
    grid-template-columns: 1fr 1fr;
    column-gap: calc(.5 * var(--pcPadding));
  }

}


</style>

