<script setup>
import ProjectCard from './ProjectCard.vue'
</script>

<template>
  <section class="p-6 md:p-8" id="projects">
    <h2
      class="mb-8 inline-block -rotate-1 border-4 border-black bg-white px-6 py-2 text-3xl font-black uppercase shadow-[6px_6px_0px_0px_rgba(0,0,0,1)] md:text-4xl"
    >
      Projects
    </h2>

    <div class="grid gap-8 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4">
      <ProjectCard
        title="FlixQuest"
        description="Android app where you can stream movies and TV shows built using Flutter, TMDB API and Firebase"
        imageUrl="/images/flixquest.png"
        :tags="['Flutter', 'Firebase', 'REST API', 'SQLite']"
        codeLink="https://github.com/BeamlakAschalew/flixquest"
        demoLink="https://flixquest.beamlak.dev"
      />
      <ProjectCard
        title="asciify"
        description="A small webapp to convert any image into ASCII characters"
        imageUrl="/images/ascii.png"
        :tags="['jQuery', 'JIMP', 'Bootstrap']"
        codeLink="https://github.com/BeamlakAschalew/asciify"
        demoLink="https://beamlak.dev/asciify"
      />
      <ProjectCard
        title="WikiTok"
        description=" A small fultter app to get a random feed of Wikipedia articles in TikTok style scrolling"
        imageUrl="/images/wikitok.png"
        :tags="['Flutter']"
        codeLink="https://github.com/BeamlakAschalew/wikitok"
      />
      <ProjectCard
        title="Ewkethub"
        description="A Udemy like webapp that instructors can upload videos for students that can be monetized"
        imageUrl="/images/ewkethub.png"
        :tags="['PHP', 'MySQL', 'jQuery']"
        codeLink="https://github.com/BeamlakAschalew/ewkethub"
        demoLink="https://ewkethub.beamlak.dev"
      />
      <ProjectCard
        title="Simon Game"
        description="JavaScript implementation of the classic Simon game"
        imageUrl="/images/simon.png"
        :tags="['JavaScript', 'jQuery']"
        codeLink="https://github.com/BeamlakAschalew/simon-game"
        demoLink="https://beamlak.dev/simon-game"
      />
    </div>
  </section>
</template>
