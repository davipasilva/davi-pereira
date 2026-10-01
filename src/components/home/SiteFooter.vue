<script setup>
import YellowButton from '@/components/ui/YellowButton.vue'
import FooterColumn from '@/components/home/FooterColumn.vue'
import amazonLogo from '@/assets/images/footer/amazon-logo.svg'
import flagBrasil from '@/assets/images/footer/flag-brasil.svg'

const columns = [
  {
    heading: 'Conheça-nos',
    items: [
      'Conheça-nos',
      'Sobre a Amazon',
      'Informações corporativas',
      'Carreiras',
      'Comunicados à imprensa',
      'Comunidade',
      'Acessibilidade',
      'Amazon Science',
    ],
  },
  {
    heading: 'Ganhe dinheiro conosco',
    items: [
      'Venda na Amazon',
      'Proteja e construa a sua marca',
      'Forneça para a Amazon',
      'Publique seus livros',
      'Seja um associado',
      'Anuncie seus produtos',
    ],
  },
  {
    heading: 'Pagamento',
    items: ['Meios de Pagamento', 'Compre com Pontos', 'Cartão de crédito Amazon'],
  },
  {
    heading: 'Deixe-nos ajudar você',
    items: [
      'Sua conta',
      'Frete e prazo de entrega',
      'Devoluções e reembolsos',
      'Gerencie seu conteúdo e dispositivos',
      'Recalls e alertas de segurança do produto',
      'Ajuda',
    ],
  },
]

const legalLinks = [
  'Condições de Uso',
  'Notificação de Privacidade',
  'Cookies',
  'Anúncios Baseados em Interesses',
]
</script>

<template>
  <footer>
    <!-- CTA: login recommendations -->
    <div class="border-t border-b border-gray-200 bg-white py-8">
      <div class="mx-auto flex max-w-[1440px] flex-col items-center gap-3 px-4 text-center">
        <p class="text-[26px] font-bold text-black">Veja recomendações personalizadas</p>
        <YellowButton label="Fazer seu login" to="/login" />
        <p class="text-[14px] text-black">
          Cliente novo?
          <RouterLink to="/login" class="text-[#265594] underline">Comece aqui</RouterLink>
        </p>
      </div>
    </div>

    <!-- Back to top -->
    <div class="bg-[#313e4f] py-4 text-center">
      <a href="#top" class="text-[16px] font-bold text-white">Voltar ao início</a>
    </div>

    <!-- Footer link columns -->
    <div class="bg-[#202936] px-4 py-10">
      <div class="mx-auto grid max-w-[1440px] grid-cols-2 gap-8 sm:grid-cols-4">
        <FooterColumn v-for="col in columns" :key="col.heading" :heading="col.heading" :items="col.items" />
      </div>
    </div>

    <!-- Language / country selector -->
    <div class="border-t border-[#3a4553] bg-[#202936] py-6">
      <div class="mx-auto flex max-w-[1440px] flex-col items-center gap-3 px-4">
        <img :src="amazonLogo" alt="Amazon" class="h-9 w-[119px]" />
        <button
          type="button"
          class="flex items-center gap-2 rounded-[3px] border border-[#797b7d] px-3 py-1.5 text-[14px] text-[#bdbebf]"
        >
          <img :src="flagBrasil" alt="Brasil" class="h-4 w-[22px]" />
          Brasil
        </button>
      </div>
    </div>

    <!-- Legal -->
    <div class="bg-[#14191f] px-4 py-6 text-center text-[14px]">
      <p class="flex flex-wrap justify-center gap-x-1 leading-[26px] text-[#d9d9d9]">
        <a v-for="link in legalLinks" :key="link" href="#" class="hover:underline">{{ link }}</a>
      </p>
      <p class="leading-[26px] text-[#d9d9d9]">© 2021-2026 Amazon.com, Inc. ou suas afiliadas</p>

      <p class="mt-3 leading-[26px] text-[#8d8d8d]">
        Amazon Serviços de Varejo do Brasil Ltda. | CNPJ 15.436.940/0001-03
      </p>
      <p class="leading-[26px] text-[#8d8d8d]">
        Av. Juscelino Kubitschek, 2041, Torre E, 18° andar - São Paulo CEP: 04543-011 |
        <a href="#" class="text-white hover:underline">Fale conosco</a>
        | ajuda-amazon@amazon.com.br
      </p>
      <p class="leading-[26px] text-[#8d8d8d]">
        Formas de pagamento aceitas: cartões de crédito (Visa, MasterCard, Elo e American Express),
        cartões de débito (Visa e Elo), Boleto e Pix.
      </p>
    </div>
  </footer>
</template>
