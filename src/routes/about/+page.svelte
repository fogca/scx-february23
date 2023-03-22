<script>
import { onMount } from "svelte";

</script>

<svelte:head>
	<title>ABOUT | 心をほどく、いたわる時間 | 焼酎屋 SHOCHU.X</title>
</svelte:head>

<main class="About l-pages">
  <section id="ab-top">
    <div class="wrapper">
      <h1 class="h1">
        伝統ある國酒 ー 焼酎を<br>
        ずっと、これからも。
      </h1>
      <p class="h4">
        焼酎は、蒸溜の技術が伝わった室町時代から続く伝統あるお酒であり、日本酒と<br class="pc">
        ともに世界に誇る日本のお酒です。特筆すべきは、その麹による蒸溜回数の少なさと、<br class="pc">
        それにより生まれた力強い香りと旨みです。
        <br><br>
        その土地の香りや空気を感じることのできる古き良きお酒、焼酎をより多くの方に<br class="pc">
        お届けしたいという想いで、焼酎にまつわる、さまざまな魅力をお伝えしてまいります。
      </p>
      <a href="/about" class="h6 l-link">わたしたちの焼酎</a>
    </div>
    <img src="./image/about.jpg" alt="">
  </section>

  <section id="ab-main">
    <div class="wrapper">
      
      <div class="l-section-head">
        <h2 class="h1">蒸溜酒における焼酎の魅力</h2>
        <p>
          世界でみられる蒸溜酒は、蒸溜を繰り返す行う連続蒸溜が一般的ですが、
          一方で焼酎は、日本独自の発展を遂げた「麹」による発酵により、アルコール度数の
          高い「醪」を取り出すことが可能です。これにより一回の蒸溜で必要十分の
          アルコール度数となり、素材の香りや旨みを感じることができるようになります。
          <br><br>
          また香りや旨み、味わい深さが強く残る焼酎は、時間の熟成により、
          まろやかさや落ち着きが生まれ、奥深さが感じ取れるようになります
        </p>
      </div>
    </div>
    <img src="./image/about.jpg" alt="">
  </section>

</main>




<style>

.l-pages {padding-top: 12.5rem;}
.About .wrapper {width: 92.5%;}
.About .wrapper p {margin: 1.5rem 0 2.5rem;}

#ab-top .wrapper {padding-bottom: 1rem;}
#ab-top .wrapper h1 {margin-left: -1px;}
#ab-top img {
  width: 100vw;
  margin-top: 6rem;
  margin-left: calc(-1 * var(--padding));
}


#ab2 {margin-top: 6rem;}

@media screen and (min-width: 720px) {
  
  .l-pages {padding-top: 20.5rem;}


  #ab-top img {
    height: 50vh;
  }

}

</style>