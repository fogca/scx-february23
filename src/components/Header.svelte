<script>
  import Saos from "saos";
  import Logo from '../components/Logo.svelte';
  import Menu from '../components/Menu.svelte';
  import gsap from 'gsap';
  import { navigating } from '$app/stores';
  import { page } from '$app/stores';
	import { onMount } from 'svelte';
  import { browser } from "$app/environment";

  onMount(() => {
    if (browser) {
      let jsheader = document.getElementsByTagName('header');
      jsheader[0].style.visibility = "visible";
    }
  });

  export let clicked = false;
	export let isExpanded = false;
	function clickHandler() {
		isExpanded = !isExpanded  
  }

  $: $page.url && (isExpanded = false);
  $: $page.url && (clicked = false);


</script>

<div>
  <!--:class="{
    'is-active': isActiveMenu, 
    'scrolled': headerHiddenFlag,
    'is-top': headerTopFlag }" -->
  <header>
    <a href="/" aria-label="Home" class="sp" data-sveltekit-reload>
      <Logo />
    </a>

    <div class="right">
      <a href="/about" class="h5 half" lang="en">About</a>
      <a href="/about" class="h5 half" lang="en">Products</a>

      <div class="menus">
        <div class="open-button sp" 
            class:clicked={clicked} 
            on:click="{() => clicked = !clicked}" 
            on:click|preventDefault={clickHandler}>
            <span></span><span></span>
          </div>
      </div>    
      <svg xmlns="http://www.w3.org/2000/svg" width="13.961" height="13.618" viewBox="0 0 13.961 13.618">
        <path id="Path_371" data-name="Path 371" d="M14.861,11.8H12.414l-.6,8.983a3.872,3.872,0,0,0,3.864,4.135H21.4a3.872,3.872,0,0,0,3.864-4.128l-.6-8.991Zm0,.774H13.142l-.55,8.263a3.1,3.1,0,0,0,3.09,3.307H21.4a3.1,3.1,0,0,0,3.1-3.307l-.558-8.263H22.218v.488a3.678,3.678,0,1,1-7.357,0Zm6.582,0H15.635v.488a2.9,2.9,0,1,0,5.808,0Z" transform="translate(-11.559 -11.55)" fill="#584527" fill-rule="evenodd"/>
        <path id="Path_371_-_Outline" data-name="Path 371 - Outline" d="M12.18,11.55H24.891l.62,9.224A4.122,4.122,0,0,1,21.4,25.168H15.682a4.122,4.122,0,0,1-4.114-4.4Zm12.243.5H12.648l-.581,8.75a3.622,3.622,0,0,0,3.614,3.869H21.4a3.622,3.622,0,0,0,3.615-3.861Zm-11.515.274h2.2v.738a3.428,3.428,0,0,0,6.857,0v-.738h2.2l.573,8.5a3.348,3.348,0,0,1-3.34,3.574H15.682a3.348,3.348,0,0,1-3.339-3.574Zm1.7.5H13.376l-.534,8.029a2.848,2.848,0,0,0,2.84,3.04H21.4a2.848,2.848,0,0,0,2.841-3.04l-.542-8.03H22.468v.238a3.928,3.928,0,1,1-7.857,0Zm.774-.5h6.308v.738a3.154,3.154,0,1,1-6.308,0Zm5.808.5H15.885v.238a2.654,2.654,0,1,0,5.308,0Z" transform="translate(-11.559 -11.55)" fill="#584527"/>
      </svg>
      
    </div>
        
      

  </header>
  
  {#if isExpanded}
    <Menu />
  {/if}
  

</div>



<style>

header {visibility: hidden;}

@keyframes -global-header-top {
	0% {transform: translateY(-.5rem);opacity: 0;}
	100% {transform: translateX(0);opacity: 1;}
}

header {
  width: 100vw;
  background-color: var(--backgroundColor);
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  position: fixed;
  top: 0;
  z-index: 99;
  padding: 1.8rem var(--padding) 1.4rem;
  border-bottom: solid 1px rgba(200, 200, 200, .5);
  border-bottom: solid .5px rgba(200, 200, 200, .5);
}

header .right {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
header .right * {margin-left: 1rem;}

</style>