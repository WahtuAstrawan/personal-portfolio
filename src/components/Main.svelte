<script>
  import Step from "./Step.svelte";

  let steps = [
      {
          name: "Memotions",
          icon: "fa-solid fa-smile",
          description:
              "A mental wellness app to support Indonesian users of all ages through personalized journaling, emotion analysis, and gamification features like streaks and achievements. The app integrates machine learning and generative AI to provide tailored feedback and insights, created with Kotlin.",
          href: "https://github.com/WahtuAstrawan/memotions-android"
      },
      {
          name: "Save & Loan",
          icon: "fa-solid fa-file-invoice-dollar",
          description:
              "An intuitive and user-friendly application for managing member savings and loans with Flutter. This application offers seamless integration with an API and robust authentication mechanisms, providing a reliable and secure financial management tool.",
          href: "https://github.com/WahtuAstrawan/saving-and-loan-app"
      },
      {
          name: "PromptSpace",
          icon: "fa-solid fa-diagram-project",
          description:
              "An innovative platform for sharing and creating AI prompts, accessible to a wide audience. Key features include tagging, search functionality, and Google OAuth integration. Developed with NextJS14, MongoDB Atlas/Mongoose, Tailwind, and NextAPI.",
          href: "https://github.com/WahtuAstrawan/promptspace"
      },
  ];

  let abouts = [
  {
    name: "a passionate developer and IT student",
    description:
      "As an undergraduate Information Technology student with a strong academic foundation, I am driven by a deep passion for web and mobile development. Through hands-on projects and rigorous coursework, I’ve honed my skills in programming, database design, and software engineering, maintaining a strong academic performance.",
  },
  {
    name: "a dedicated problem solver and innovator",
    description:
      "I thrive on solving real-world challenges by building innovative applications like the Memotions mental wellness app and AI prompt-sharing platform. My ability to design and implement comprehensive systems showcases my commitment to creating impactful and user-friendly solutions.",
  },
  {
    name: "an enthusiastic learner and communicator",
    description:
      "My journey includes learning diverse technologies such as Kotlin, React, and Flutter, and earning certifications in Android Development and Software Engineering. I also prioritize clear communication and teamwork, contributing to successful project execution and strong professional relationships.",
  },
];
</script>

<main class="flex flex-col flex-1 p-4">
  <section
      id="introPage"
      class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"
  >
      <div
          class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
      >
          <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
              Hi! I'm <span class="poppins text-violet-400">Wahtu Astrawan</span> 
              <br />Web and Mobile
              <span class="poppins text-violet-400">Developer</span>
          </h2>
          <p class="text-base sm:text-lg md:text-xl">
            An IT undergraduate passionate about web and mobile development, <span class="text-violet-400"> I specialize in creating web applications using Javascript
            and mobile app using Kotlin</span>
          </p>
          <a href="assets/CV_I Gusti Ngurah Putu Astrawan.pdf" download="CV_I Gusti Ngurah Putu Astrawan.pdf">
            <button
                class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950"
            >
                <div
                    class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
                ></div>
                <h4 class="relative z-9">Download CV</h4>
            </button>
          </a>
      </div>
      <div class="relative shadow-2xl grid place-items-center">
          <img
              src={"images/profile.png"}
              alt="Wahtu Astrawan"
              class="object-cover z-[2] max-h-[120vh] pb-24"
          />
      </div>
  </section>
  <section class="py-20 lg:py-32 flex flex-col gap-24" id="projects">
      <div class="flex flex-col gap-2 text-center">
          <h6 class="text-large sm:text-xl md:text-2xl">
              A few of my creative endeavors.
          </h6>
          <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
              Curious to <span class="poppins text-violet-400">see</span> my work?
          </h3>
      </div>
      <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
        {#each steps as step, index}
            <Step step={step}>
                <p>
                  {step.description}
                </p>
            </Step>
        {/each}
      </div>
  </section>
  <section
      id="about"
      class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
  >
      <div
          class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
      >
          <h6 class="text-large sm:text-xl md:text-2xl">
              Want to know more?
          </h6>
          <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
              A bit <span class="poppins text-violet-400">about</span> me.
          </h3>
      </div>
      <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
          {#each abouts as about, index}
              <div class="flex gap-6 sm:gap-8">
                  <p
                      class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold"
                  >
                      0{index + 1}
                  </p>
                  <div class="flex flex-col gap-6 sm:gap-8">
                      <h3 class="text-2xl sm:text-3xl md:text-5xl">
                          {about.name}
                      </h3>
                      <p>{about.description}</p>
                  </div>
              </div>
          {/each}
      </div>
  </section>
</main>