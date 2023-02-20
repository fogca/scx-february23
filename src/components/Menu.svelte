<script>
    import Logo from './Logo.svelte'
    import { blur, fade, slide, fly } from 'svelte/transition';
    import { expoInOut, expoOut, sineInOut, sineOut } from 'svelte/easing';
</script>
    
    <div class="Menu" 
        in:fade={{ delay: 500, duration: 1200, easing: sineInOut }}
        out:fade={{ delay: 0, duration: 1200, easing: sineInOut }}
    >  
    <div class="MenuWrapper">
    <div class="wrapper">
        <!--<li in:fly={{ y: 10, delay: 0, duration: 2500, easing: expoInOut }}></li>-->
        <li 
            in:fade={{ delay: 1500, duration: 1800, easing: sineOut }}
        >
            <a href="/works" >
                <h1 lang="en" class="h4 uppercase">デザインとスタイリング</h1>
                <span class="h4">Design and styling</span>
            </a>
        </li>

        <li in:fade={{ delay: 1500, duration: 2000, easing: sineOut }}>
            <a href="/products">
                <h1 lang="en" class="h4 uppercase">手掛けたプロダクト</h1>
                <span class="h4">Product collections</span>
            </a>
        </li>

        <li in:fly={{ delay: 1500, duration: 2000, easing: sineOut }}>
            <a href="/about" >
                <h1 lang="en" class="h4 uppercase">エトセトラについて</h1>
                <span class="h4">About etcetera inc.</span>
            </a>
        </li>

        <li in:fly={{ delay: 1500, duration: 2000, easing: sineOut }}>
            <a href="/contact" >
                <h1 lang="en" class="h4 uppercase">お問い合わせはこちら</h1>
                <span class="h4">Get in touch with us</span>
            </a>
        </li>


    </div>
    <div class="container" in:fly={{ delay: 1500, duration: 2000, easing: sineOut }}>
        <h3 class="h5">
            <span class="first">et cetera inc.</span><br>
            <span class="second">18-23 B1F Oyamacho Shibuya-ku</span><br>
            <span class="last">Tokyo 151-0065 Japan</span>
        </h3>
        <h4 class="h5 semitrans" lang="en">©︎ 2022 et cetera inc.</h4>
    </div>

    </div>
</div>

<style>

/*
.Menu .wrapper h2 {font-size: 2.8rem;}
*/

.Menu {
    width: 100vw;
    height: 100vh;
    height: 100svh;
    background-color: var(--backgroundColor);
    position: fixed;
    z-index: 98;
    padding-left: var(--padding);
}

.MenuWrapper {
    position: relative;
    height: 100%;
}

.Menu .wrapper {margin-top: 15rem;}
.Menu .wrapper a {
    display: block; 
    margin-bottom: 4.2rem;
}

.Menu a h1 {
    font-size: 1.35rem;
    margin-left: -1.2px;
}
.Menu a span {
    font-size: 1.2rem;
    opacity: .5;
}

.Menu .container {
    position: absolute;
    bottom: 15%;
    transform: translateY(-100%);
}

.Menu .container span.second {margin-left: -1.4px;}
.Menu .container span.last {margin-left: -.5px;}
.Menu .container h4 {margin-top: 0.5rem;}

</style>