<script>
  export let y;

  export let tabs = [
    { name: "Projects", link: "#projects" },
    { name: "About me", link: "#about" },
  ];
</script>

<header
  class={"sticky top-0 z-[10] flex items-center justify-between border-b border-solid px-6 duration-200 " +
    (y > 0
      ? " border-blue-950 bg-slate-950 py-4"
      : " border-transparent bg-transparent py-6")}
>
  <h1 class="font-medium">
    <b class="quicksand font-bold">Noah</b>
    <span>Trần</span>
  </h1>
  <div class="ml-auto hidden items-center gap-4 pr-4 sm:flex">
    {#each tabs as tab, index}
      <a
        href={tab.link}
        class="duration-200 hover:text-cyan-400"
        target={index === 2 ? "_blank" : ""}
      >
        <p>{tab.name}</p>
      </a>
    {/each}
  </div>
  <a href="https://www.instagram.com/noah_tran1109/" target="_blank">
    <button
      class="blueShadow group relative overflow-hidden rounded-full bg-white px-5 py-2 text-slate-950"
    >
      <div
        class="absolute right-full top-0 z-0 h-full w-full bg-blue-400 opacity-20 duration-200 group-hover:translate-x-full"
      />
      <h4 class="z-9 relative">Get in touch</h4>
    </button>
  </a>
</header>
