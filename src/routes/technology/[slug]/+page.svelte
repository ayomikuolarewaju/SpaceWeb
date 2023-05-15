<script> 
  import Nav from '../../../components/nav.svelte';
  import img1 from '$lib/img/bgtech.jpg';
  import img2 from '$lib/img/background-destination-mobile.jpg';
 

  import {page} from '$app/stores';
  console.log($page)
  let slug= $page.params.slug
  console.log(slug)

  export let data;
  let techs = data.technology;
  console.log(techs)
   let tech = techs.filter((cw)=>cw.id === slug)
   console.log(tech)
 
 
  </script>
  

<div class="flex flex-col w-full h-full bg-no-repeat  items-start relative overflow-hidden justify-between" style="background-image: url('{img1}');">
    <Nav/>

    <div class="container flex flex-col text-white my-auto mx-auto md:p-10 w-3/3 relative md:-top-20 
    overflow-hidden space-x-20  ">
        <div class="pl-20">
            <small class="pl-20">THE TERMINOLOGY......</small>
        </div>
        <div class="pb-5 pl-20">
            <h5 class="capitalize text-5xl">{tech[0].name}</h5>
        </div>
        <div class="pb-5 md:w-1/3 w-2/3 pl-20">
          <p>{tech[0].description}</p>
      </div>
    </div>
    <div class="flex flex-col absolute z-50 text-white md:items-center md:mx-auto md:left-16 space-y-10 top-40">
        {#each techs as crw (crw.id)}
        <a data-sveltekit-reload 
        class="pb-8 pt-8 space-x-10 hover:bg-white rounded-full p-10 border-white border-2"
         href="/technology/{crw.id}">
            {crw.id}</a>
        {/each}
    </div>
    <div class="container md:flex md:flex-col text-white items-start space-x-40 hidden
    p-5 w-full mx-auto my-auto absolute space-y-10 top-16 -right-96 pr-20 justify-center overflow-hidden">
        <h5 class=" text-xl pt-14 relative left-36 ">03 SPACE LAUNCH 101</h5>
        <img src="{tech[0].images.portrait}" alt="" width="500" height="500" class="overflow-hidden">
    </div>
</div>