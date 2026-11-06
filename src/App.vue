<script setup>
const liens = [
  { titre: 'À propos', href: '#a-propos' },
  { titre: 'Projets', href: '#projets' },
  { titre: 'Contact', href: '#contact' },
]

// Ajoute un objet ici pour ajouter une carte de projet
const projets = [
  { titre: 'Civilisation Minecraft Divergente', description: 'Plugin Minecraft Civilisation modulaire', url: '#' },
  { titre: 'Apprentissage COBOL autodidacte', description: 'Petites applications COBOL', url: '#' },
]
</script>

<template>
  <!-- En-tête -->
  <header class="border-b border-bordure">
    <nav class="mx-auto flex max-w-3xl flex-wrap items-center justify-between gap-2 px-6 py-4">
      <a href="#" class="font-semibold">Florian Senicourt</a>
      <ul class="flex gap-6 text-sm text-discret">
        <li v-for="lien in liens" :key="lien.href">
          <a :href="lien.href" class="hover:text-accent">{{ lien.titre }}</a>
        </li>
      </ul>
    </nav>
  </header>

  <main class="mx-auto max-w-3xl px-6">
    <!-- Présentation -->
    <section class="py-20">
      <p class="text-sm font-medium text-accent">Bonjour, je suis</p>
      <h1 class="mt-2 text-4xl font-bold tracking-tight sm:text-5xl">Florian Senicourt</h1>
      <p class="mt-4 max-w-xl text-lg text-discret">
        Apprenti technicien informatique, développeur de plugin Minecraft à mes heures perdues.
      </p>
      <a href="#projets" class="mt-8 inline-block rounded-lg bg-accent px-5 py-2.5 text-sm font-medium text-white hover:opacity-90">
        Voir mes projets
      </a>
    </section>

    <!-- À propos -->
    <section id="a-propos" class="scroll-mt-8 border-t border-bordure py-16">
      <h2 class="text-2xl font-bold tracking-tight">À propos</h2>
      <p class="mt-4 text-discret">
        Actuellement en 2e année de BUT Informatique à l'IUT de Calais, j'ai commencé ma deuxième année en apprentissage chez DillingerFrance en tant qu'"Assistant Technicien d'Exploitation Informatique/Helpdesk". J'ai intégré un parcours Administration de systèmes et réseaux et j'ai pour objectif de faire une école d'Ingénieur après mon BUT, dans le but de devnir Architecte réseau. Je suis passionné par l'informatique, et bien que je suive la voie du réseau, le développement m'intéresse aussi tout particulièrement.
      </p>
    </section>

    <!-- Projets -->
    <section id="projets" class="scroll-mt-8 border-t border-bordure py-16">
      <h2 class="text-2xl font-bold tracking-tight">Projets</h2>
      <div class="mt-6 grid gap-6 sm:grid-cols-2">
        <article v-for="projet in projets" :key="projet.titre" class="rounded-xl border border-bordure bg-white p-6">
          <h3 class="font-semibold">{{ projet.titre }}</h3>
          <p class="mt-2 text-sm text-discret">{{ projet.description }}</p>
          <a :href="projet.url" class="mt-4 inline-block text-sm font-medium text-accent hover:underline">Voir le projet</a>
        </article>
      </div>
    </section>

    <!-- Contact -->
    <section id="contact" class="scroll-mt-8 border-t border-bordure py-16">
      <h2 class="text-2xl font-bold tracking-tight">Contact</h2>
      <p class="mt-4 text-discret">
        Retrouve-moi sur
        <a href="https://github.com/flobanai" class="font-medium text-accent hover:underline">GitHub</a>
        <a href="https://www.linkedin.com/in/florian-senicourt/" class="font-medium text-accent hover:underline">LinkedIn</a>
        <a href="mailto:floriansenicourt@gmail.com" class="font-medium text-accent hover:underline">Email</a>.
      </p>
    </section>
  </main>

  <!-- Pied de page -->
  <footer class="border-t border-bordure">
    <p class="mx-auto max-w-3xl px-6 py-6 text-sm text-discret">© 2026 Florian Senicourt</p>
  </footer>
</template>
