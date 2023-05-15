<script> 

  import Nav from '../components/nav.svelte';
import img1 from '$lib/img/background-home-desktop.jpg';
import img2 from '$lib/img/background-home-mobile.jpg';
import img3 from '$lib/img/background-home-tablet.jpg';
import img4 from '$lib/img/bg.png';


</script>

<div class="flex flex-col w-full h-full bg-no-repeat  items-start relative overflow-hidden" style="background-image: url('{img1}');">
    <Nav/>

    <div class="container flex flex-col text-white my-auto p-10 space-y-5 md:w-1/3 absolute top-52 w-full md:left-40">
        <h2>SO,YOU WANT TO TRAVEL TO</h2>
        <h6 class="text-7xl leading-normal">SPACE</h6>
        <p class="">
            So, you want to travel to Space Let’s face it; 
            if you want to go to space, you might as well 
            genuinely go to outer space and not hover kind 
            of on the edge of it. Well sit back, and relax
            because we’ll give you a truly out of this
            world experience! Explore
        </p>
    </div>
    <div class="text-black bg-white rounded-full items-center p-11 hidden md:block
    mx-auto my-auto absolute w-60 h-60 bottom-28 right-80 overflow-hidden">
       <p class=" text-4xl pt-14 pr-5 ">EXPLORE</p>
   </div>


</div>

