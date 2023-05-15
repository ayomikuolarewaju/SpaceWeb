<script>
    import logo from '$lib/img/logo.svg';
</script>

<div class="flex flex-row items-start w-full mx-auto relative">
    
    <div >
        <img src="{logo}" alt="" class="p-5">
    </div>
    <div class="absolute left-28 z-30">
        <hr class=" hidden h-px my-8 bg-white border-0 w-80 md:flex md:flex-col">
    </div>
    
    <div class="md:flex md:flex-row bg-slate-700 text-white w-2/3 justify-between hidden
     text-sm items-center mx-auto my-auto pl-20 pr-20 rounded-sm absolute right-20">
      <a class="hover:border-b-4 hover:border-white pb-8 pt-8" href="/">00 HOME</a>
      <a class="hover:border-b-4 hover:border-white pb-8 pt-8" href="/destination/Moon">01 DESTINATION</a>
      <a class="hover:border-b-4 hover:border-white pb-8 pt-8" href="/crew/1">02 CREW</a>
      <a class="hover:border-b-4 hover:border-white pb-8 pt-8" href="/technology/A">03 TECHNOLOGY</a>
    </div>
    <div class="md:hidden flex flex-row text-white w-2/3 
     text-sm pl-5 pr-5 rounded-sm absolute left-32 top-5 space-x-6">
      <a class="hover:border-b-4 hover:border-white pb-4 pt-4" href="/">00 HOME</a>
      <a class="hover:border-b-4 hover:border-white pb-4 pt-4" href="/destination/Moon">01 DESTINATION</a>
      <a class="hover:border-b-4 hover:border-white pb-4 pt-4" href="/crew/1">02 CREW</a>
      <a class="hover:border-b-4 hover:border-white pb-4 pt-4" href="/technology/A">03 TECHNOLOGY</a>
    </div>
</div>