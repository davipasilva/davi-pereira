<script setup>
import closeIcon from '@/assets/images/nav-drawer/close-icon.svg'
import accountIcon from '@/assets/images/nav-drawer/account-icon.svg'

defineProps({
  open: {
    type: Boolean,
    default: false,
  },
})

defineEmits(['close'])

const sections = [
  {
    heading: 'Destaques',
    items: ['Mais Vendidos', 'Novidades na Amazon', 'Produtos em alta'],
  },
  {
    heading: 'Conteúdo digital e dispositivos',
    items: [
      'Amazon Fire TV',
      'Amazon Music',
      'Prime Video',
      'Aplicativos Amazon',
      'Dispositivos Kindle e eBooks',
      'Echo e Alexa',
      'Audiolivros Audible',
    ],
  },
  {
    heading: 'Comprar por categoria',
    items: ['Alimentos e Bebidas', 'Automotivo', 'Bebês', 'Beleza e Cuidados Pessoais'],
  },
]
</script>

<template>
  <Teleport to="body">
    <Transition enter-active-class="transition-opacity duration-200" leave-active-class="transition-opacity duration-200" enter-from-class="opacity-0" leave-to-class="opacity-0">
      <div v-if="open" class="fixed inset-0 z-50 bg-black/82" @click="$emit('close')">
        <Transition enter-active-class="transition-transform duration-200" leave-active-class="transition-transform duration-200" enter-from-class="-translate-x-full" leave-to-class="-translate-x-full">
          <div v-if="open" class="flex h-full w-fit" @click.stop>
            <aside class="flex h-full w-[347px] flex-col overflow-y-auto bg-white">
              <div class="flex h-[47px] shrink-0 items-center gap-4 bg-[#202936] px-6">
                <img :src="accountIcon" alt="" class="size-6 shrink-0" />
                <p class="text-[20px] font-bold text-white">Olá, faça seu login</p>
              </div>

              <nav class="divide-y divide-gray-200">
                <div v-for="section in sections" :key="section.heading" class="px-6 py-4">
                  <p class="text-[18px] font-bold text-[#1e1e1e]">{{ section.heading }}</p>
                  <a v-for="item in section.items" :key="item" href="#" class="block text-[14px] leading-[36px] text-[#1e1e1e] hover:underline">
                    {{ item }}
                  </a>
                </div>
              </nav>
            </aside>

            <button type="button" aria-label="Fechar menu" class="mt-4 ml-4 size-[17px] shrink-0" @click="$emit('close')">
              <img :src="closeIcon" alt="" class="size-full" />
            </button>
          </div>
        </Transition>
      </div>
    </Transition>
  </Teleport>
</template>
