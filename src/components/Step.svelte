<script>
  export let step;
</script>

<a
  href={step.href}
  target="_blank"
  class="group flex cursor-pointer flex-col gap-4 rounded-lg border border-solid border-blue-700 p-4 text-center duration-200 hover:border-cyan-400 sm:p-6 md:p-8"
>
  <div
    class="mx-auto -mt-10 grid place-items-center bg-slate-950 px-4 text-5xl duration-200 sm:-mt-12 md:-mt-14 md:text-6xl lg:-mt-16"
  >
    <i class={step.icon} />
  </div>
  <h3 class="text-xl font-medium sm:text-2xl md:text-3xl">
    {step.name}
  </h3>
  <slot />
  <div class="justify-betweeen flex flex-1 items-end gap-4">
    <div
      class="relative ml-auto cursor-pointer overflow-hidden duration-200 after:absolute after:right-full after:top-0 after:z-[-1] after:h-full after:w-full after:bg-white after:duration-200 hover:text-slate-950 hover:after:translate-x-full"
    >
      <p class="z-4">Go to &rarr;</p>
    </div>
  </div>
</a>
