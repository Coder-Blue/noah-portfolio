<script>
  import Step from "./Step.svelte";

  let steps = [
    {
      name: "Zircon AI App",
      icon: "fa-regular fa-message",
      href: "https://github.com/Coder-Blue/zircon-app-op",
    },
    {
      name: "Argon Note App",
      icon: "fa-regular fa-note-sticky",
      href: "https://argon-note.vercel.app/",
    },
    {
      name: "Natri Social Media",
      icon: "fa-solid fa-globe",
      href: "https://natri-soc.vercel.app/",
    },
  ];

  let benefits = [
    {
      metric: "10x",
      name: "a self taught developer",
      description:
        "I taught myself to code using free online resources and absolutely fell in love with the creativity and problem solving that is involved in developing and engineering innovative new online experiences. Currently all of my works and researchs are quite decent in the JavaScript Ecosystem. And I won't be hesitate to learn new things everyday.",
    },
    {
      name: "a product design & UX finatic",
      description:
        "I always want my user to have a good looking UI app on their screen. So I'm a careful guy when choosing a design language for my apps. A guarantee for a harmony and symmetrical design UI/UX for users.",
    },
    {
      name: "an excellent communicator",
      description:
        "I'm a Vietnamese. But I can use English as my second language fluently. I believe communication is key and it's a paramount value of mine. During problem solving process, my communication skill will come in handy to help with the team's project, and a essential part for creating a good colleague relationship in any workspace.",
    },
  ];
</script>

<main class="flex flex-1 flex-col p-4">
  <section
    id="introPage"
    class="grid grid-cols-1 gap-10 py-8 sm:py-14 lg:grid-cols-2"
  >
    <div
      class="flex flex-col gap-6 text-center md:gap-8 lg:justify-center lg:gap-10 lg:text-left"
    >
      <h2 class="text-4xl font-semibold sm:text-5xl md:text-6xl">
        Hi! I'm <span class="quicksand text-blue-400">Noah</span> Trần
        <br />An <strong class="text-violet-600"> Asexual</strong> Full Stack
        <span class="quicksand text-blue-400">Developer</span>
      </h2>
      <p class="text-base sm:text-lg md:text-xl">
        My <span class="text-blue-400">favorite tech</span> includes
        <span class="text-yellow-400"> JavaScript </span>
        (NEXT.JS, SvelteKit, Vite or RSBuild), TailwindCSS, shadcn/ui, Node.js, Bun.js,
        Express.js && PostgresSQL or Google Firebase/Firestore! <br /><br /> And
        <span class="text-orange-400"> Rust</span>, mostly Tauri, Tauri Mobile.
      </p>
      <a
        href="https://www.instagram.com/noah_muted/"
        target="_blank"
        class="blueShadow quicksand group relative mx-auto overflow-hidden rounded-full bg-white px-6 py-3 text-base text-slate-950 sm:text-lg md:text-xl lg:ml-0 lg:mr-auto"
      >
        <div
          class="absolute right-full top-0 z-0 h-full w-full bg-blue-400 opacity-20 duration-200 group-hover:translate-x-full"
        />
        <h4 class="z-9 relative">Get in touch &rarr;</h4>
      </a>
    </div>
    <div class="relative grid place-items-center shadow-2xl">
      <img
        src={"images/profile.png"}
        alt="Profile Noah IMG"
        loading="lazy"
        class="z-[2] max-h-[70vh] object-cover"
      />
    </div>
  </section>

  <section id="projects" class="flex flex-col gap-24 py-20 lg:py-32">
    <div class="flex flex-col gap-2 text-center">
      <h6 class="text-lg sm:text-xl md:text-2xl">
        A few of my creative endeavors.
      </h6>
      <h3 class="text-3xl font-semibold sm:text-4xl md:text-5xl">
        Curious to <span class="quicksand text-blue-400">see</span> my works?
      </h3>
    </div>
    <div class="grid grid-cols-1 gap-12 lg:grid-cols-3 lg:gap-10">
      <Step step={steps[0]}>
        <p>
          Zircon AI App is an AI chatbot app created with <strong
            class="text-blue-400"
          >
            Vite React and Tauri</strong
          >. Using Google Gemini AI API as the brain. Aim to help many teachers
          who want to use AI but have a low end PC.
        </p>
      </Step>
      <Step step={steps[1]}>
        <p>
          A fullstack clone of Notion created with <strong
            class="text-blue-400"
          >
            Next.js, Convex, Shadcn/ui</strong
          >. Using a powerful techstack, aim for a high performance but simple
          to use for everyone.
        </p>
      </Step>
      <Step step={steps[2]}>
        <p>
          A clone of Instagram created with <strong class="text-blue-400">
            RSBuild React and Firebase</strong
          >. A simple to use social media app. Still in beta.
        </p>
      </Step>
    </div>
  </section>

  <section
    id="about"
    class="relative flex flex-col gap-16 py-20 pt-10 sm:gap-20 md:gap-24 lg:py-32 lg:pt-16"
  >
    <div
      class="relative flex flex-col gap-2 py-4 text-center before:absolute before:left-0 before:top-0 before:h-1.5 before:w-2/3 before:bg-blue-700 after:absolute after:bottom-0 after:right-0 after:h-1.5 after:w-2/3 after:bg-blue-700"
    >
      <h6 class="text-large sm:text-xl md:text-2xl">Want to know more?</h6>
      <h3 class="text-3xl font-semibold sm:text-4xl md:text-5xl">
        A bit <span class="quicksand text-blue-400">about</span> me.
      </h3>
    </div>
    <p class="quicksand mx-auto text-lg font-semibold sm:text-xl md:text-2xl">
      I am . . .
    </p>
    <div class="mx-auto flex w-full max-w-[800px] flex-col gap-20">
      {#each benefits as benefit, index}
        <div class="flex gap-6 sm:gap-8">
          <p
            class="poppins text-4xl font-semibold text-cyan-500 sm:text-5xl md:text-6xl"
          >
            0{index + 1}
          </p>
          <div class="flex flex-col gap-6 sm:gap-8">
            <h3 class="text-2xl sm:text-3xl md:text-5xl">
              {benefit.name}
            </h3>
            <p>{benefit.description}</p>
          </div>
        </div>
      {/each}
    </div>
    <h5 class={" poppins text-center text-2xl font-semibold sm:text-3xl "}>
      The <span class="text-blue-400">Complete</span> Package
    </h5>
    <div
      class="mx-auto flex w-full max-w-[800px] flex-col gap-10 overflow-x-scroll"
    >
      <table class="rounded bg-white text-center text-slate-700">
        <thead class={"border-b border-solid border-slate-200  "}>
          <tr class="">
            <th />
            <th class="whitespace-nowrap p-2 px-4">Candidate #1</th>
            <th class="whitespace-nowrap p-2 px-4">Candidate #2</th>
            <th class="whitespace-nowrap p-2 px-4">Candidate #3</th>
            <th class="whitespace-nowrap bg-blue-700 p-4 px-8 text-white">Me</th
            >
          </tr>
        </thead>
        <tbody>
          <tr class="border-b border-solid border-slate-200">
            <td
              class="border-r border-solid border-white py-4 pl-4 pr-8 text-sm font-semibold"
              >Dedication</td
            >
            <td><i class="fa-solid fa-xmark text-slate-500" /></td>
            <td><i class="fa-solid fa-check text-slate-500" /></td>
            <td><i class="fa-solid fa-xmark text-slate-500" /></td>
            <td><i class="fa-solid fa-check text-green-500" /></td>
          </tr>
          <tr class="border-b border-solid border-slate-200">
            <td
              class="border-r border-solid border-white py-4 pl-4 pr-8 text-sm font-semibold"
              >Critical Thought</td
            >
            <td><i class="fa-solid fa-xmark text-slate-500" /></td>
            <td><i class="fa-solid fa-check text-slate-500" /></td>
            <td><i class="fa-solid fa-check text-slate-500" /></td>
            <td><i class="fa-solid fa-check text-green-500" /></td>
          </tr>
          <tr>
            <td
              class="border-r border-solid border-white py-4 pl-4 pr-8 text-sm font-semibold"
              >Interpersonal Skills</td
            >
            <td><i class="fa-solid fa-check text-slate-500" /></td>
            <td><i class="fa-solid fa-check text-slate-500" /></td>
            <td><i class="fa-solid fa-xmark text-slate-500" /></td>
            <td><i class="fa-solid fa-check text-green-500" /></td>
          </tr>
          <tr class="border-t border-solid border-slate-200">
            <td
              class="border-r border-solid border-white py-4 pl-4 pr-8 text-sm font-semibold"
              >Programming Ability</td
            >
            <td><i class="fa-solid fa-check text-slate-500" /></td>
            <td><i class="fa-solid fa-xmark text-slate-500" /></td>
            <td><i class="fa-solid fa-check text-slate-500" /></td>
            <td><i class="fa-solid fa-check text-green-500" /></td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="mx-auto -mt-12 italic opacity-50 sm:hidden">
      <p>Scroll to see more &rarr;</p>
    </div>
    <p class="mx-auto">So why not invest?</p>
  </section>
</main>
