<script> 
  import Nav from '../../../components/nav.svelte';
  import img1 from '$lib/img/bgcrew.jpg';
  import img2 from '$lib/img/background-destination-mobile.jpg';
  import img6 from '$lib/img/image-mars.png';

  import {page} from '$app/stores';
  console.log($page)
  let slug= $page.params.slug
  console.log(slug)

  export let data;
  let crew = data.crews;
  console.log(crew)
   let crw = crew.filter((cw)=>cw.id === slug)
   console.log(crw)
 
 
  </script>
  

<div class="flex flex-col w-full h-full bg-no-repeat  items-start relative overflow-hidden" style="background-image: url('{img1}');">
    <Nav/>

    <div class="container flex flex-col text-white md:my-auto md:mx-auto md:p-10 md:w-3/3 relative md:-top-20 overflow-hidden
    top-20 space-y-10 w-full p-5">
    
        <div class="md:pb-5">
            <h5 class="text-2xl">{crw[0].role}</h5>
        </div>
        <div class="md:pb-5 space-y-5">
          <h5 class="text-5xl">{crw[0].name}</h5>
      </div>
      <div class="md:w-1/3 w-full md:pb-5 space-y-5">
          <p>{crw[0].bio}</p>
      </div>
    </div>
    <div class="absolute z-50 text-white items-center mx-auto left-16 space-x-10 bottom-12">
        {#each crew as crw (crw.id)}
        <a data-sveltekit-reload class="bg-white  rounded-full p-2" href="/crew/{crw.id}">
            {crw.id}</a>
        {/each}
    </div>
    <div class="container md:flex md:flex-col text-white items-start w-full space-x-40 p-5
    hidden mx-auto my-auto absolute space-y-10 top-28 -right-96 pr-20">
        <h5 class=" text-xl pr-5 relative left-36 overflow-hidden">02 MEET YOUR CREW</h5>
        <img src="{crw[0].images.png}" alt="" width="400" height="400" class="overflow-hidden">
    </div>
</div>