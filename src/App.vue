<script setup>
import Navbar from './components/TheNavbar.vue'
import AboutMe from './components/AboutMe.vue'
import Projects from './components/TheProjects.vue'
import Skills from './components/TheSkills.vue'
import Experience from './components/TheExperience.vue'
import TechStack from './components/TechStack.vue'
import ContactForm from './components/ContactForm.vue'
import Footer from './components/TheFooter.vue'

import { Globe, Server, Database, Smartphone, Zap, Code } from 'lucide-vue-next'

const navItems = [
  { name: 'Home', href: '#' },
  { name: 'Projects', href: '#projects' },
  { name: 'Skills', href: '#skills' },
  { name: 'Experience', href: '#experience' },
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
    year: '2022 - Present',
    title: 'Senior Full Stack Developer at Tech Innovators',
    description:
      'Leading development of cloud-based SaaS products. Architected microservices infrastructure and mentored junior developers.',
    color: 'bg-blue-300',
  },
  {
    year: '2020 - 2022',
    title: 'Full Stack Developer at Digital Solutions Inc.',
    description:
      'Developed and maintained e-commerce platforms and content management systems for enterprise clients.',
    color: 'bg-green-300',
  },
  {
    year: '2018 - 2020',
    title: 'Frontend Developer at Creative Agency',
    description:
      'Created responsive web applications and interactive user interfaces for various clients in retail and finance sectors.',
    color: 'bg-yellow-300',
  },
]

const techStack = [
  { name: 'Vue', color: 'bg-green-300', rotate: 'rotate-2' },
  { name: 'Nuxt.js', color: 'bg-gray-200', rotate: '-rotate-1' },
  { name: 'TypeScript', color: 'bg-blue-400', rotate: 'rotate-1' },
  { name: 'Node.js', color: 'bg-green-400', rotate: '-rotate-2' },
  { name: 'Express', color: 'bg-gray-300', rotate: 'rotate-1' },
  { name: 'MongoDB', color: 'bg-green-300', rotate: '-rotate-1' },
  { name: 'PostgreSQL', color: 'bg-blue-300', rotate: 'rotate-2' },
  { name: 'GraphQL', color: 'bg-pink-300', rotate: '-rotate-2' },
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
      <TechStack :techStack="techStack" />
      <ContactForm />
    </main>
    <Footer :navItems="navItems" />
  </div>
</template>
