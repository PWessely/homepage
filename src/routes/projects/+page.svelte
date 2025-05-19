<script>
  const projects = [
    {
      name: 'My Portfolio Website',
      desc: 'This very site: built with SvelteKit, Tailwind, and interactive components.',
      tags: ['SvelteKit', 'Tailwind', 'JavaScript'],
      link: '/'
    },
    {
      name: 'Pharma Data Model',
      desc: 'Machine learning project for a pharmaceutical company optimizing dosage predictions.',
      tags: ['Python', 'Data Science', 'ML'],
      link: '#'
    },
    {
      name: 'Manufacturing Optimization',
      desc: 'Data science model to improve machine efficiency for an industrial client.',
      tags: ['Python', 'Optimization'],
      link: '#'
    }
  ];
</script>

<h1 class="text-3xl font-bold mb-6">Projects</h1>
<div class="grid gap-8 md:grid-cols-2">
  {#each projects as p}
    <a href={p.link} class="block p-6 bg-white rounded-xl shadow hover:shadow-lg transition">
      <h2 class="text-2xl font-semibold mb-2">{p.name}</h2>
      <p class="text-gray-600 mb-4">{p.desc}</p>
      <div class="flex flex-wrap gap-2">
        {#each p.tags as tag}
          <span class="bg-blue-100 text-blue-800 text-xs font-medium px-2.5 py-0.5 rounded">{tag}</span>
        {/each}
      </div>
    </a>
  {/each}
</div>