<script>
  import { dev } from "$app/environment";
  import { inject } from "@vercel/analytics";
  import SvelteSeo from "svelte-seo";
  import Header from "../components/Header.svelte";
  import Footer from "../components/Footer.svelte";
  import "../app.css";

  inject({ mode: dev ? "development" : "production" });

  let y;
  let innerWidth = 0;
  let innerHeight = 0;

  function goTop() {
    document.body.scrollIntoView();
  }
</script>

<SvelteSeo
  title="Noah Trần's Svelte Portfolio"
  description="The Personal SvelteKit Portfolio website of Trần Ngô Anh Quân/Noah Trần/Sh1ro"
  keywords="Noah Trần, SvelteKit, Tailwindcss, JavaScript, Portfolio, ParticlesJS"
  canonical="https://noah-sh1ro.vercel.app/"
  author="Noah Trần"
  openGraph={{
    title: "Noah Trần.dev",
    description:
      "Just a silly portfolio developed with SvelteKit, JavaScript & ParticlesJS.",
    url: "https://noah-sh1ro.vercel.app/",
    image: "https://i.ibb.co/VNTs6tF/og-noah.jpg",
    type: "website",
    site_name: "Noah Trần.dev",
  }}
  twitter={{
    card: "summary_large_image",
    site: "@not_sh1ro",
    title: "Noah Trần's Svelte Portfolio",
    description:
      "The Personal SvelteKit Portfolio website of Trần Ngô Anh Quân/Noah Trần/Sh1ro",
    image: "https://i.ibb.co/VNTs6tF/og-noah.jpg",
  }}
/>

<div
  class="relative mx-auto flex min-h-screen w-full max-w-[1400px] flex-col text-sm sm:text-base"
>
  <div
    class={"fixed bottom-0 z-[10] flex w-full p-10 duration-200" +
      (y > 0
        ? " opacity-full pointer-events-auto"
        : " pointer-events-none opacity-0")}
  >
    <button
      on:click={goTop}
      class="ml-auto grid aspect-square cursor-pointer place-items-center rounded-full bg-slate-900 px-3 text-blue-400 hover:bg-slate-800 sm:px-4"
    >
      <i class="fa-solid fa-arrow-up" />
    </button>
  </div>
  <Header {y} />
  <slot />
  <Footer />
</div>

<svelte:window bind:scrollY={y} bind:innerHeight bind:innerWidth />
