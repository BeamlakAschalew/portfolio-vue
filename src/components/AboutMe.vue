<script setup>
import { Github, Linkedin, Mail } from 'lucide-vue-next'
</script>

<template>
  <div class="relative overflow-hidden p-6 md:p-8">
    <!-- Background elements -->
    <div
      class="absolute -right-20 top-10 h-40 w-40 rotate-12 rounded-lg bg-yellow-400 md:h-64 md:w-64"
    ></div>
    <div
      class="absolute -left-10 bottom-10 h-32 w-32 -rotate-12 rounded-lg bg-pink-400 md:h-48 md:w-48"
    ></div>

    <div class="relative z-10 mx-auto max-w-4xl">
      <div
        class="mb-8 rotate-1 transform rounded-lg border-4 border-black bg-white p-6 shadow-[8px_8px_0px_0px_rgba(0,0,0,1)] transition-all hover:-rotate-1 hover:shadow-[12px_12px_0px_0px_rgba(0,0,0,1)] md:p-10"
      >
        <h2
          class="mb-6 inline-block -rotate-1 border-4 border-black bg-black px-6 py-2 text-3xl font-black uppercase text-white shadow-[4px_4px_0px_0px_rgba(0,0,0,1)] md:text-4xl"
        >
          About Me
        </h2>

        <div class="flex flex-col gap-6 md:flex-row">
          <!-- Profile Photo -->
          <div class="w-full max-w-[300px] md:w-1/3 mx-auto md:mx-0">
            <div
              class="rotate-2 border-4 border-black bg-white p-2 shadow-[6px_6px_0px_0px_rgba(0,0,0,1)]"
            >
              <img
                src="/images/avatar.jpg"
                alt="Profile Photo"
                class="h-full w-full object-cover border-2 border-black aspect-square"
              />
            </div>
          </div>

          <!-- About Text -->
          <div class="md:w-2/3">
            <p class="mb-4 text-lg font-bold">
              Selam (Hello)! I am Beamlak Aschalew, passionate Full Stack and mobile app Developer
              with over 5 years of experience building high quality softwares.
            </p>

            <p class="mb-4 font-medium">
              I specialize in creating responsive, user-friendly applications using modern
              technologies like Vue, and Laravel. My approach combines technical expertise with
              creative problem-solving to deliver solutions that exceed expectations.
            </p>

            <p class="mb-6 font-medium"></p>

            <div class="flex flex-wrap gap-4">
              <a
                href="#projects"
                class="-rotate-2 border-4 border-black bg-green-400 px-6 py-6 text-lg font-black text-black shadow-[6px_6px_0px_0px_rgba(0,0,0,1)] transition-all hover:rotate-0 hover:bg-green-500 hover:shadow-[8px_8px_0px_0px_rgba(0,0,0,1)]"
              >
                View Projects
              </a>

              <a
                href="/beamlak_aschalew_cv.pdf"
                target="_blank"
                class="-rotate-2 border-4 border-black bg-blue-400 px-6 py-6 text-lg font-black text-black shadow-[6px_6px_0px_0px_rgba(0,0,0,1)] transition-all hover:rotate-0 hover:bg-blue-500 hover:shadow-[8px_8px_0px_0px_rgba(0,0,0,1)]"
              >
                Download Resume
              </a>

              <div class="flex gap-3">
                <a
                  href="https://github.com/BeamlakAschalew"
                  class="flex items-center justify-center h-14 w-14 rotate-3 border-4 border-black bg-white shadow-[4px_4px_0px_0px_rgba(0,0,0,1)] transition-all hover:rotate-0 hover:bg-gray-100 hover:shadow-[6px_6px_0px_0px_rgba(0,0,0,1)]"
                >
                  <Github class="h-6 w-6 mx-auto" />
                </a>
                <a
                  href="https://et.linkedin.com/in/beamlak-aschalew-a0866622b"
                  class="flex items-center justify-center h-14 w-14 -rotate-2 border-4 border-black bg-white shadow-[4px_4px_0px_0px_rgba(0,0,0,1)] transition-all hover:rotate-0 hover:bg-gray-100 hover:shadow-[6px_6px_0px_0px_rgba(0,0,0,1)]"
                >
                  <Linkedin class="h-6 w-6 mx-auto" />
                </a>
                <a
                  href="mailto:beamlakaschalew.19@gmail.com"
                  class="flex items-center justify-center h-14 w-14 rotate-1 border-4 border-black bg-white shadow-[4px_4px_0px_0px_rgba(0,0,0,1)] transition-all hover:rotate-0 hover:bg-gray-100 hover:shadow-[6px_6px_0px_0px_rgba(0,0,0,1)]"
                >
                  <Mail class="h-6 w-6 mx-auto" />
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
