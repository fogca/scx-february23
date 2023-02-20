<script>
import { onMount } from "svelte";

</script>

<svelte:head>
	<title>About | etc inc. - Space direction</title>
</svelte:head>

<main class="About l-pages">
  <section id="ab1">
    <div class="wrapper">
      <h1 class="h1">
        消費する焼酎から、<br>
        豊かさを添える、愉しむ焼酎へ。
      </h1>
      <p class="h4">
        本文はデザインや全体のボリューム感を確認するためのダミーテキストです。校正が終了した際は、文章をこちらから置き換えてください。ダミーテキストとして、ぜひご活用ください。
        <br><br>
        本文はデザインや全体のボリューム感を確認するためのダミーテキストです。校正が終了した際は、文章をこちらから置き換えてください。
      </p>
      <a href="/about" class="h6 l-link">わたしたちの焼酎</a>
    </div>
    <img src="./image/about.jpg" alt="">
  </section>

  <section id="ab2">
    <div class="wrapper">
      <h2 class="h2">蒸溜酒における焼酎の魅力</h2>
      <p>
        わたしたちは、日本の蒸溜酒である焼酎を大切に、そして、その魅力を形にしお届けいたします。ぜひ、OOな焼酎をお愉しみください。
        <br><br>
        わたしたちは、日本の蒸溜酒である焼酎を大切に、そして、その魅力を形にしお届けいたします。ぜひ、OOな焼酎をお愉しみください。
      </p>
    </div>
    <img src="./image/about.jpg" alt="">
  </section>

</main>




<style>

.l-pages {padding-top: 14.5rem;}
.About .wrapper {width: 85%;}
.About .wrapper p {margin: 1.5rem 0 2.5rem;}

#ab1 .wrapper {padding-bottom: 1rem;}
#ab1 .wrapper h1 {margin-left: -1px;}
#ab1 img {
  width: 100vw;
  margin-top: 6rem;
  margin-left: calc(-1 * var(--padding));
}


#ab2 {margin-top: 6rem;}

@media screen and (min-width: 720px) {
  

}

</style>