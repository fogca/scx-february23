<script>
import Logo from '../components/Logo.svelte';
</script>

<footer>
    <div class="about">
        <a href="/" class="footer-logo">
            <Logo />
        </a>
        
        <p class="h4">
            わたしたちは、日本の蒸溜酒である<br>
            焼酎を大切に、そして、その魅力を形にし、<br>
            お届けいたします。<br>
            <br>
            ゆったりお愉しみいただける焼酎を<br>
            ご堪能ください。わたしたちは、日本の蒸溜酒<br>
            である焼酎を大切に、そして、その魅力を形にし、<br>
            お届けいたします。
        </p>
    </div>
    <div class="pages">
        <a href="/" class="container">
            <h2 class="h4">わたしたちが目指す姿</h2>
            <h3 class="h5 half" lang="en">About Us / Our Vision</h3>
        </a>
        <a href="/" class="container">
            <h2 class="h4">わたしたちの考える焼酎</h2>
            <h3 class="h5 half" lang="en">Our Products</h3>
        </a>
        <a href="/" class="container">
            <h2 class="h4">焼酎の愉しみ方</h2>
            <h3 class="h5 half" lang="en">Shochu Cocktails</h3>
        </a>
    </div>
    <div class="links">
        <ul class="jp-links">
            <li><a href="/" class="h5">会社概要</a></li>
            <li><a href="/" class="h5">よくある質問</a></li>
            <li><a href="/" class="h5">お問い合わせ</a></li>
            <li><a href="/" class="h5">ニュースレター</a></li>
            <li><a href="/" class="h5">キャンセル・返金</a></li>          
        </ul>
        <ul class="en-links">
            <li><a href="/" lang="en" class="h4">Instagram</a></li>
            <li><a href="/" lang="en" class="h4">note</a></li>
            <li><a href="/" lang="en" class="h4">Podcast</a></li>
            <li><a href="/" lang="en" class="h4">Twitter</a></li>
            <li><a href="/" lang="en" class="h4">LINE Official</a></li>          
        </ul>
    </div>
    <div class="l-line"></div>
    <div class="bottom">
        <div class="h6" lang="en">©SHOCHU.X</div>
        <div class="right">
            <a href="/" class="h6" lang="en">Legal</a>
            <a href="/" class="h6" lang="en">Privacy Policy</a>
        </div>
    </div>
</footer>


<style>
    footer a {display: block;}
    footer {
        margin-top: 8rem;
        padding: 0 var(--padding);
        padding-top: 8rem;
        padding-bottom: 1.2rem;
        background-color: var(--footerColor);
    }
    footer .footer-logo {width: 10.5rem;}
    footer .about p {margin-top: 3rem;}

    footer .pages {margin-top: 6rem;}
    footer .pages a {margin-top: 2.5rem;}

    footer .links {
        margin-top: 5rem;
        display: flex;
    }
    footer .links ul {width: 48%;}
    footer .links li {margin-bottom: 1.5rem;}
    footer .l-line {
        margin: 4rem 0 1.5rem;
        margin-left: calc(-1 * var(--padding));
        opacity: .5;
    }
    
    footer .bottom {
        display: flex;
        justify-content: space-between;
        opacity: .5;
    }
    footer .bottom .right a {
        display: inline-block;
        margin-left: 2rem;
    }
    
</style>