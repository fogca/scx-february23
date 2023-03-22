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
	<title>心をほどく、いたわる時間 | 焼酎屋 SHOCHU.X</title>
  <script src="https://webfont.fontplus.jp/accessor/script/fontplus.js?kqbwQX--jVA%3D&box=bYUqUdOYlP4%3D&aa=1&ab=2"></script>
</svelte:head>


<main> 

<section id="in-top">
  <div class="wrapper">

    <div class="visual">
      <img src="../image/nagomi-pc.webp" alt="">
    </div>
    <div class="tagline">
      <h1 class="h2">心をほどく、いたわる時間</h1>
      <p>
        酔うお酒から、ゆっくり自己と向き合うお酒に。<br>
        夜が楽しみになる、そんな焼酎をお届けいたします。<br>
        余韻が響く私たちのお酒を、ぜひご堪能ください。
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
      わたしたちのお酒を、多くの方の手に取っていただき<br>
      お楽しみいただけるよう、焼酎の魅力や飲み方を<br>
      共有するイベントやセミナーを開催しております。
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
  <div class="wrapper l-products">

    <a href="/" class="container">
      <img src="../image/kizuna.jpg" alt="">
      <h2 class="h2">全麹三段仕込みの麦焼酎「希継奈」</h2>
      <p class="h5 half">『全麹三段仕込み』製法により、甘みとコクが存分に引き出された原酒を5年間熟成することで、</p>
      <div class="bottom">
        <div class="h3 price" lang="en">¥6,800</div>
        <div class="h4 l-buy">購入する</div>
      </div>
    </a>
    <a href="/" class="container">
      <img src="../image/nagomi.jpg" alt="">
      <h2 class="h2">全麹三段仕込みの麦焼酎「希継奈」</h2>
      <p class="h5 half">『全麹三段仕込み』製法により、甘みとコクが存分に引き出された原酒を5年間熟成することで、</p>
      <div class="bottom">
        <div class="h3 price" lang="en">¥6,800</div>
        <div class="h4 l-buy">購入する</div>
      </div>
    </a>
    <a href="/" class="container">
      <img src="../image/kiraboshi.jpg" alt="">
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
      <h2 class="h1">そのほかの<br>私たちのお酒</h2>
      <h3 lang="en">Products</h3>
      <p class="pc">
        私たちは、「希継奈」や「和深」、「煌星」のほかにも<br>
        熟成に重きをおいたシリーズや現在準備中のお酒も<br>
        ございますので、ぜひ楽しみにお待ちください。
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
      <img src="../image/@product.jpg" alt="">
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
      <img src="../image/@product.jpg" alt="">
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
      <img src="../image/@product.jpg" alt="">
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
        <img src="../image/@product.jpg" alt="">
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
          <img src="../image/@product.jpg" alt="">
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
    <img src="../image/@cocktails.jpg" alt="">
    <h2 class="h1">ゆったりと<br>焼酎カクテルを愉しむ</h2>
    <h3 lang="en">Shochu Cocktail</h3>
    <p class="pc">焼酎は、さまざまなバーでみかけるお酒ー蒸溜酒の
      一つであり、ストレートで頂く以外にもたくさんの
      愉しみ方があります。私たちの蒸溜酒は、アルコール
      度数も高く、さまざまなシーンでお愉しみいただけます。</p>
  </div>
  <div class="wrapper col-2">
    
    <a href="/" class="container">
      <img src="../image/@cocktail_1.jpg" alt="">
      <h3 class="h3">焼酎香るレモンサワー</h3>
      <div class="h6 half" lang="en">Lemon Sour</div>
      <p class="h5 opacity">焼酎の力づよい香りに、爽やかな檸檬がキレを表現し、<br>
        食卓をフレッシュに彩るロングカクテルです。
      </p>
      <a href="/" class="l-link">記事を詳しく</a>
    </a>

    <a href="/" class="container">
      <img src="../image/@cocktail_2.jpg" alt="">
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
  <div class="wrapper">
    <div class="l-section-head">
      <h2 class="h1">取り扱い店舗のご紹介</h2>
      <h3 lang="en">Introduce our partners</h3>
      <p>
        焼酎カルチャー発信地の九州は勿論のこと、東京や大阪、<br>
        そのほか多くの地域にてお取り扱いいただいています。<br>
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
    <a href="/" class="h5 l-link">ほかの店舗も確認する</a>
  </div>
</section>


<section id="in-link">
  <div class="wrapper col-2">
    <div class="container">
      <div class="l-section-head">
        <h2 class="h1">発酵と蒸溜、そして熟成</h2>
        <h3 lang="en">Fermentation, distillation and aging</h3>
        <p>
          焼酎は、日本の麹が生み出した、独自の発展を遂げた蒸溜酒です。<br class="pc">
          その独特の香りは、原料や発酵、その蒸溜方法から作り出されます。<br class="pc">
          伝統ある、焼酎の歴史や製造の風景を、ぜひご覧ください。
        </p>
      </div>
      <a href="/" class="h5 l-link">すべて読む</a>
    </div>
    <div class="container">
      <div class="l-section-head">
        <h2 class="h1">想いを共にする仲間</h2>
        <h3 lang="en">Partner distillery</h3>
        <p>
          焼酎への熱い想いを共にする、酒造の方々にご協力いただき、<br class="pc">
          これまで六本の焼酎を、皆様にお届けすることができました。<br class="pc">
          その想いや、各酒造の哲学、わたしたちが目指す姿をまとめました。
        </p>
      </div>
      <a href="/" class="h5 l-link">すべて読む</a>
    </div>
  </div>
</section>


<section id="in-archive">
  <div class="l-section-head">
    <img src="../image/cocktail.jpeg" alt="">
    <h2 class="h1">飲み比べを通して<br>愉しみ方をシェア</h2>
    <h3 lang="en">Event / Workshop</h3>
    <p class="pc">
      わたしたちは、焼酎の魅力や愉しみ方を共有する場として、
      さまざまなバーや百貨店、コミュニティにて
      セミナーやワークショップを開催しております。アーカイブを
      まとめてありますので、ぜひご覧ください。</p>
  </div>
  <div class="wrapper col-2">
    
    <a href="/" class="container">
      <img src="../image/@cocktail_1.jpg" alt="">
      <h3 class="h3">湯割りと燗酎</h3>
      <div class="h6 half" lang="en">at Nihonbashi SOIL</div>
      <p class="h5 opacity">焼酎の力づよい香りに、爽やかな檸檬がキレを表現し、<br>
        食卓をフレッシュに彩るロングカクテルです。
      </p>
      <a href="/" class="l-link">記事を詳しく</a>
    </a>

    <a href="/" class="container">
      <img src="../image/@cocktail_2.jpg" alt="">
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
  <img src="../image/@product.jpg" alt="">
  <div class="wrapper">
    <div class="section-head">
      <h2 class="h2">ニュースレター</h2>
      <p>
        焼酎の魅力やその奥深さ、また限定イベントのお知らせを
        ニュースレターを通して、告知させていただく場合もございます。
      </p>
    </div>
    <form action="">
      <input class="h4" type="email" name="contact[email]" aria-label="メールアドレス" placeholder="メールアドレス">
      <button class="h4">登録</button>
    </form>
  </div>
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
    height: calc(100vh - (4rem + 2rem + (1.5rem * 1.8 + 3.6rem * 1.9 + 1.0rem * 1.8 + 2rem)));
    height: calc(100dvh - (4rem + 2rem + (1.5rem * 1.8 + 3.6rem * 1.9 + 1.0rem * 1.8 + 2rem)));
    margin-bottom: 4rem;
  }
  #in-top .wrapper .visual img {
    width: 100vw;
    margin-left: calc(-1 * var(--padding));
    height: 100%;}
  #in-top .wrapper .tagline p {
    font-size: 1.1rem;
    margin: 1rem 0 2.0rem;
    margin-left: .5px;
    opacity: .75;
    line-height: 2.2;
  }
  #in-top .wrapper .tagline a {margin-left: 1.4px;}
  


  #in-news {margin-top: 4rem;}
  #in-news .wrapper {margin-top: 3rem;}
  #in-news .l-link {margin-top: 3.5rem;}




  #in-product {margin-top: 10rem;}

  
  #in-product .carousel {
    width: 100vw;
    margin-left: calc(-1 * var(--padding));
    margin-top: 3rem;
  }
  #in-product .carousel h1 {
    margin-left: var(--padding);
    margin-bottom: 2rem;
  }

  #in-product .carousel .container {
    width: 100%;
    margin-bottom: 5rem;
  }
  #in-product .carousel .container p {width: 92.5%;}
  #in-product .carousel .container .bottom {
    margin-top: 1.5rem;
    padding-right: .5rem;
  }

  #in-cocktail {margin-top: 10rem;}

  #in-cocktail .wrapper .container h3 {
    margin: 2rem 0 0.5rem;
    font-size: 1.6rem;
  }
  #in-cocktail .wrapper .container p {margin: 1rem 0 4rem;}

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
  #in-link .l-section-head {margin-bottom: 2rem;}
  #in-link .container {margin-bottom: 10rem;}


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


  #in-archive {display: none;}



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
  #in-top .wrapper .visual img {margin-left: 0;}

  #in-top .wrapper .tagline {
    position: absolute;
    z-index: 1;
    bottom: 8rem;
    top: auto;
    opacity: .9;
  }
  #in-top .wrapper .tagline * {color: var(--backgroundColor);}


  #in-news {margin-top: 16rem;}
  #in-news .l-section-head {margin-top: 3rem;}
  #in-news .wrapper {overflow: hidden;}

  #in-product {
    margin-top: 14.5rem;
  }
  #in-product .l-section-head {width: 30vw;}

  #in-product .container img {height: calc((70vw - var(--pcPadding) * 1) / 3 / 16 * 9);}
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
  #in-product .carousel .container {
    width: 18.5vw;
    margin-bottom: 8rem;
  }
  #in-product .carousel .container h2 {font-size: 1.3rem;}
  #in-product .carousel .container h3, 
  #in-product .carousel .container .l-buy {display: none;}



  #in-cocktail {margin-top: 0;}
  #in-cocktail .l-section-head h2,
  #in-archive .l-section-head h2 {margin-top: 16rem;}
  #in-cocktail .wrapper {margin-top: 8rem;}

  #in-cocktail .l-section-head p,
  #in-archive .l-section-head p {width: calc((100vw - var(--padding) * 2.5) / 2);}

  #in-shop {
    margin-top: 24rem;
    padding-bottom: 10rem;
  }
  #in-shop .wrapper {margin-top: 8rem;}
  #in-shop .l-section-head {width: 30vw;}
  #in-shop img {height: 50vh;}
  #in-shop .wrapper {
    display: flex;
    justify-content: flex-start;
    align-items: flex-start;
    flex-wrap: wrap;
  }
  #in-shop .wrapper .container {
    width: calc(100vw - var(--pcPadding)*2 - 30vw);
    margin-top: 4.5rem;
    padding-left: var(--pcPadding);
  }
  #in-shop .wrapper .container a {width: 27.5%;}


  #in-link {margin: 20rem 0 18rem;}
  #in-link .l-section-head {margin-bottom: 4rem;}
  #in-link .l-section-head h3 {margin: 1rem 0 2rem;}
  #in-link .container {margin-bottom: 0;}


  #in-mail {
    height: 62.5vh;
    height: 62.5dvh;
    margin-top: 16rem;
  }
  
  #in-mail .wrapper {
    width: 50%;
    max-height: 80%;
    padding: 8rem 10% 6rem;
    background-color: rgba(255, 255, 255, 0.9);
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  #in-mail .wrapper form {margin-top: 4rem;}
  #in-mail img, #in-mail .wrapper {position: absolute;} 
  #in-mail img:nth-of-type(1) {
    margin-top: 0;
    margin-left: calc(-1 * var(--pcPadding));
    height: 100%;
  }
  #in-mail img:nth-of-type(2) {display: none;}


}


</style>

