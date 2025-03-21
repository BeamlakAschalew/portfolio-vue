<script setup>
import Navbar from './components/TheNavbar.vue'
import AboutMe from './components/AboutMe.vue'
import Projects from './components/TheProjects.vue'
import Skills from './components/TheSkills.vue'
import Experience from './components/TheExperience.vue'
import Education from './components/TheEducation.vue'
import TechStack from './components/TechStack.vue'
import ContactForm from './components/ContactForm.vue'
import Footer from './components/TheFooter.vue'

import { Globe, Server, Database, Smartphone, Zap, Code } from 'lucide-vue-next'

const navItems = [
  { name: 'Home', href: '#' },
  { name: 'Projects', href: '#projects' },
  { name: 'Skills', href: '#skills' },
  { name: 'Experience', href: '#experience' },
  { name: 'Education', href: '#education' },
  { name: 'Contact', href: '#contact' },
]

const skills = [
  {
    name: 'Frontend',
    icon: Globe,
    color: 'bg-yellow-300',
    items: ['Vue', 'JavaScript', 'jQuery', 'TypeScript', 'Tailwind CSS'],
  },
  {
    name: 'Backend',
    icon: Server,
    color: 'bg-blue-300',
    items: ['Laravel', 'Node.js', 'Express', 'Firebase'],
  },
  {
    name: 'Database',
    icon: Database,
    color: 'bg-green-300',
    items: ['MySQL', 'SQLite', 'SQL Server', 'Eloquent'],
  },
  {
    name: 'Mobile',
    icon: Smartphone,
    color: 'bg-purple-300',
    items: ['Flutter'],
  },
  {
    name: 'DevOps',
    icon: Zap,
    color: 'bg-red-300',
    items: ['CI/CD', 'GitHub Actions'],
  },
  {
    name: 'Languages',
    icon: Code,
    color: 'bg-pink-300',
    items: ['PHP', 'JavaScript', 'TypeScript', 'Dart', 'C#', 'Java', 'C++'],
  },
]

const experience = [
  {
    year: 'October 2023 - Present',
    title: 'Freelancing',
    description: 'Freelancing by building professional mobile apps, websites and webapps.',
    color: 'bg-blue-300',
  },
  {
    year: 'July 2023 - October 2023',
    title: 'Mobile app Developer at Micro Sun and Solutions.',
    description: 'Developed and maintained mobile apps for various clients.',
    color: 'bg-green-300',
  },
]

const education = [
  {
    year: '2023 - 2027',
    title: 'HiLCoE School of Computer Science and Technology.',
    description: 'Learning Software Engineering.',
    color: 'bg-blue-300',
  },
]

const techStack = [
  { name: 'Flutter', color: 'bg-purple-300', rotate: 'rotate-1' },
  { name: 'Laravel', color: 'bg-red-300', rotate: '-rotate-2' },
  { name: 'MySQL', color: 'bg-yellow-300', rotate: 'rotate-2' },
  { name: 'SQLite', color: 'bg-blue-300', rotate: '-rotate-1' },
  { name: 'SQL Server', color: 'bg-green-300', rotate: 'rotate-1' },
  { name: 'Tailwind CSS', color: 'bg-teal-300', rotate: '-rotate-2' },
  { name: 'Vue', color: 'bg-green-300', rotate: 'rotate-2' },
  { name: 'TypeScript', color: 'bg-blue-400', rotate: 'rotate-1' },
  { name: 'Node.js', color: 'bg-green-400', rotate: '-rotate-2' },
  { name: 'Express', color: 'bg-gray-300', rotate: 'rotate-1' },
]
</script>

<template>
  <div class="min-h-screen bg-white">
    <Navbar :navItems="navItems" />
    <main>
      <AboutMe />
      <Projects />
      <Skills :skills="skills" />
      <Experience :experience="experience" />
      <Education :education="education" />
      <TechStack :techStack="techStack" />
      <ContactForm />
    </main>
    <Footer :navItems="navItems" />
  </div>
</template>
