<script>
import { page } from '$app/stores';
import PageTransition from '../components/PageTransition.svelte'; 
import Header from '../components/Header.svelte';
import Footer from '../components/Footer.svelte';
import { navigating } from '$app/stores';
import { onMount } from 'svelte';
import { browser } from '$app/environment';
import { goto, afterNavigate, beforeNavigate } from '$app/navigation';


/** @type {import('./$types').LayoutData} */
    export let data;
    $: currentRoute = $page.url.pathname;

</script>
  
<svelte:head>
  <link rel="stylesheet" href="../css/base.css?var=1.12">
  <link rel="stylesheet" href="../css/layout.css?var=1.12">
  <link rel="stylesheet" href="../css/prerendering.css?var=1.12">
  <link rel="stylesheet" href="https://use.typekit.net/frp6udl.css">
  <script>
    (function(d) {
      var config = {
        kitId: 'ybz8pts',
        scriptTimeout: 3000,
        async: true
      },
      h=d.documentElement,t=setTimeout(function(){h.className=h.className.replace(/\bwf-loading\b/g,"")+" wf-inactive";},config.scriptTimeout),tk=d.createElement("script"),f=false,s=d.getElementsByTagName("script")[0],a;h.className+=" wf-loading";tk.src='https://use.typekit.net/'+config.kitId+'.js';tk.async=true;tk.onload=tk.onreadystatechange=function(){a=this.readyState;if(f||a&&a!="complete"&&a!="loaded")return;f=true;clearTimeout(t);try{Typekit.load(config)}catch(e){}};s.parentNode.insertBefore(tk,s)
    })(document);
  </script>
</svelte:head>
  
  <div 
    class:Index={currentRoute === "/"} 
    class:Products={currentRoute === "/products"}
    class:Works={currentRoute === "/works"}
    class:About={currentRoute === "/about"} 
    class:Contact={currentRoute === "/contact"}
  >
    <Header />
    <PageTransition pathname={data.pathname}>
    <slot />
    </PageTransition>
    <Footer />
  </div>
  