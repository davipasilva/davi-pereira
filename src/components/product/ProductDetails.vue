<script setup>
const specs = [
  { label: 'Idioma', value: 'Português' },
  { label: 'Dimensões da embalagem', value: '22,2 x 21,9 x 10,9 cm; 1,61 quilogramas' },
  { label: 'Certificação', value: '00556-25-04083' },
  { label: 'Data de lançamento', value: '5 junho 2025' },
  { label: 'ASIN', value: 'B0F67B2D45' },
  { label: 'País de origem', value: 'Brasil' },
  {
    label: 'Ranking dos mais vendidos',
    value: 'Nº 10 em Games e Consoles (Conheça o Top 100 na categoria Games e Consoles)',
  },
]

const bestsellerRankLink = { text: 'Nº 1 em Consoles do Nintendo Switch 2', href: '#' }

const description =
  'O Nintendo Switch 2 representa a próxima evolução dos consoles, oferecendo uma experiência de jogo imersiva com gráficos aprimorados e funcionalidades inovadoras. Com resolução de até 4K na TV e suporte a HDR, os jogos ganham vida. Os novos controles Joy-Con 2 com conectores magnéticos e modo mouse expandem suas opções de interação. Conecte-se com amigos através do GameChat, compartilhando tela e fazendo chamadas de vídeo. A tela maior e os três modos de jogo proporcionam flexibilidade para jogar onde e como quiser, garantindo diversão ininterrupta. Prepare-se para a evolução da série Mario Kart em Mario Kart World para Nintendo Switch 2! O mundo inteiro é sua pista de corrida nesta experiência de mundo aberto, onde você pode correr livremente por paisagens deslumbrantes, enfrentando até 24 pilotos em emocionantes modos de jogo como Grande Prêmio e Eliminatória. Modos de jogo compatíveis: - Modo TV: Conecte-se à sua TV e desfrute de seus jogos favoritos em glorioso 4K. - Modo Semiportátil: Utilize o suporte integrado para jogar com os Joy-Con destacáveis, ideal para sessões multijogador rápidas. - Modo Portátil: Leve o Switch 2 para onde quiser e desfrute de uma experiência de console completa na palma da sua mão.'
</script>

<template>
  <section>
    <div class="border-t border-[#e0e0e0] px-[18px] py-8">
      <h2 class="text-[22px] font-bold text-black">Detalhes do produto</h2>
      <dl class="mt-4 space-y-2 pl-5 text-[14px] text-black">
        <div v-for="spec in specs" :key="spec.label" class="flex gap-1">
          <dt class="font-bold">{{ spec.label }}:</dt>
          <dd>{{ spec.value }}</dd>
        </div>
        <div>
          <a :href="bestsellerRankLink.href" class="text-[#265594] hover:underline">{{ bestsellerRankLink.text }}</a>
        </div>
      </dl>
    </div>

    <div class="border-t border-[#e0e0e0] px-[18px] py-8">
      <h2 class="text-[22px] font-bold text-black">Descrição do produto</h2>
      <p class="mt-4 pl-5 text-[13px] leading-[20px] text-[#2d2d2d]">{{ description }}</p>
    </div>

    <div class="border-t border-[#e0e0e0] px-[18px] pt-8">
      <h2 class="text-[22px] font-bold text-black">Do fabricante</h2>
    </div>
  </section>
</template>
