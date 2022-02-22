<template>
  <div id="app" class="flex flex-col bg-white">
    <div class="w-full px-2 md:px-0 container mx-auto">
      <h1 class="font-title leading-none text-3xl md:text-4xl pt-5 pb-8 md:pb-12">Monocle</h1>
      <section>
        <h1 class="text-sm md:text-4xl">
          Minimalistic and <span class="highlight"> productivity-focused</span>
          <br />
          news reader
        </h1>
        <div class="flex flex-row mt-8">
          <button
            class="w-28 md:w-56 py-1 text-sm md:text-xl rounded bg-gray-900 text-gray-100 border border-gray-900 shadow tracking-widest"
          >
            BUY
          </button>
          <button
            class="w-28 md:w-56 py-1 text-sm md:text-xl ml-2 md:ml-4 rounded bg-white text-gray-900 border border-gray-900 tracking-wide"
          >
            Import OPML
          </button>
        </div>
        <small class="text-xs text-gray-500 pt-4"
          ><b>$49</b> one time payment</small
        >
        <img src="./assets/images/ltpt.png" class="w-1/2 md:w-2/5 mx-auto mt-6 md:mt-0" alt="" />

        <section class="flex flex-col items-center justify-center text-center">
          <p class="text-sm md:text-lg">
            Stop endlessly scrollig the web.<br />
            start your
            <span class="font-bold highlight">information diet</span> right now.
          </p>
          <button
            class="tracking-widest w-36 md:w-56 py-1 text-sm md:text-xl rounded bg-gray-900 text-gray-100 border shadow mt-4"
          >
            BUY NOW
          </button>
          <small class="text-xs text-gray-500">$49 one time payment</small>
        </section>
      

      <section class="flex flex-row flex-wrap mt-16 w-full md:w-4/5 mx-auto">
        <div
          class="w-2/4 md:w-1/3 px-2 md:px-4 py-4 md:py-8 flex flex-col justify-center md:justify-start items-center text-center md:text-left" 
          v-for="(feature, index) in features"
          :key="index"
        >
          <img :src="feature.icon" class="w-8 h-6 self-center md:self-start ml-0 md:ml-6" alt="" />
          <h3 class="mt-4 font-semibold text-xs md:text-sm md:text-xl self-center md:self-start ml-0 md:ml-7">{{ feature.title }}</h3>
          <p class="mt-2 feature-text leading-tight font-normal text-xs md:text-sm">{{ feature.text }}</p>
        </div>
      </section>
      </section>

      <section
        class="flex flex-col items-center justify-center text-center mt-16 "
      >
        <p class="text-sm md:text-lg">
          <span class="font-bold highlight">Stay up to date</span> with blogs,
          newspapers, <br />
          Youtube channels and any site with a field
        </p>
        <button
          class="tracking-wide w-36 md:w-56 py-1 text-sm md:text-xl rounded bg-gray-900 text-gray-100 border shadow mt-4"
        >
          START
        </button>
        <small class="text-xs text-gray-500"
          >No monthly costs, pay <b>$49</b></small
        >
      </section>
    </div>

    <footer class="bg-gray-800 mt-16">
      <div
        class="container mx-auto flex flex-row justify-between items-center px-1 md:px-0 py-8 text-gray-500"
      >
        <div>
          <h1 class="font-title text-xl md:text-3xl leading-none">Monocle</h1>
          <small class="font-thin text-xs md:text-sm">
            by
            <a
              href="https://www.tomasmartty.com"
              target="_blank"
              class="font-normal"
              >Tomas Martty
            </a>
            from
            <a
              href="https://www.mountainlab.com"
              target="_blank"
              class="font-bold"
              >MountainLab</a
            >
          </small>
        </div>
        <div>
          <ul class="text-right text-xs md:text-sm font-thin">
            <li>Contact</li>
            <li>Privacy Policy</li>
            <li>Terms of Service</li>
          </ul>
        </div>
      </div>
    </footer>
  </div>
</template>
<script>
export default {
  name: "App",
  data() {
    return {
      features: [
        {
          icon: "./imgs/desktop-solid.svg",
          title: "Desktop First",
          text: "Take back control of your time and read only on you desktop, dont let news follow you on your phone",
        },

        {
          icon: "./imgs/eye-solid.svg",
          title: "Distraction-free",
          text: "No ads, No suggested links, No clickbait.You decide what content to follow and when to check for updates",
        },
        {
          icon: "./imgs/file-solid.svg",
          title: "Respect News Sources",
          text: "Read articles in thier original format and websites we dont want to steal traffic with in-app readers",
        },
        {
          icon: "./imgs/user-solid.svg",
          title: "Improve Productivity",
          text: "Spend less time wandering around. Read updates you care about and then go nback to work",
        },
        {
          icon: "./imgs/clock-solid.svg",
          title: "Read Later",
          text: "Cant read something right now? use monocle browser extension to save content for later",
        },
        {
          icon: "./imgs/heart-solid.svg",
          title: "Support Microprenuers",
          text: "Monocle was created and is maintained by a single developer. Whose gaol is sustainability not growth",
        },
      ],
    };
  },
};
</script>

<style>
.highlight {
  position: relative;
}
.highlight:after {
  content: "";
  position: absolute;
  top: 5px;
  left: 0;
  opacity: 0.1;
  background: #742a2a;
  width: 100%;
  height: 90%;
  transform: skewX(-10deg);
}
.feature-text {
  width: 250px;
}

@media screen and (max-width: 768px) {
  .feature-text {
    width: 101px;
  }
  
}

</style>
