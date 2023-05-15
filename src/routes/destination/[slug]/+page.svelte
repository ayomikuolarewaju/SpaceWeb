<script> 
  import Nav from '../../../components/nav.svelte';
  import img1 from '$lib/img/background-destination-desktop.jpg';
  import img2 from '$lib/img/background-destination-mobile.jpg';
  import img6 from '$lib/img/image-mars.png';
  
  import {page} from '$app/stores';
  console.log($page)
  let slug = $page.params.slug
  console.log(slug)

  export let data;
  let destination = data.destinations;
   let dest = destination.filter((dest)=>dest.name ===slug)
   console.log(dest)
   console.log(dest[0].images.png)
 
  </script>
  

<div class="flex flex-col w-full h-full bg-no-repeat  items-start relative overflow-hidden" style="background-image: url('{img1}');">
    <Nav/>

    <div class="container hidden md:flex md:flex-col text-white items-start p-11 w-full mx-auto left-40
    my-auto absolute space-y-10 top-16 overflow-hidden">
        <h5 class=" text-xl pt-14 pr-5 overflow-hidden">01 PICK YOUR DESTINATION</h5>
        <img src="{dest[0].images.png}" alt="" width="300" height="300" class="overflow-hidden">
    </div>
    <div class="relative z-50 text-white md:space-x-10 md:top-20 md:w-full items-center md:left-96 md:pl-96
    top-20 left-32 space-x-10">
        {#each destination as dest (dest.name)}
        <a data-sveltekit-reload class="hover:border-b-4 hover:border-white pb-8 pt-8" href="/destination/{dest.name}">
            {dest.name}</a>
        {/each}
    </div>

    <div class="container flex flex-col text-white my-auto mx-auto md:p-10 md:w-3/3 relative md:-bottom-10 md:left-96 md:pl-80
    top-10 left-2 space-x-10 p-20 ">
    
      <div class="pb-5">
          <h5 class="text-7xl">{dest[0].name}</h5>
      </div>
      <div class="md:w-1/3 pb-5 w-full">
          <p>{dest[0].description}</p>
      </div>
      <div class="">
        <hr class="h-px my-8 bg-white border-0 w-80">
      </div>
      <div class="container flex flex-row md:w-1/3 w-full">
          <div class="container flex flex-col">
              <small>AVG. DISTANCE</small>
              <p>{dest[0].distance}</p>
          </div>
          <div class="container flex flex-col">
              <small>EST. TRAVEL TIME</small>
              <p>{dest[0].travel}</p>
          </div>
      </div>
    </div>
 
</div>