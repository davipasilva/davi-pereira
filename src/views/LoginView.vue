<script setup>
import amazonLogo from '@/assets/images/login/amazon-logo.svg'
</script>

<template>
  <main class="min-h-screen bg-white">
    <div class="flex flex-col items-center px-4 pt-8">
      <RouterLink to="/" class="flex items-end gap-1">
        <img :src="amazonLogo" alt="Amazon" class="h-[38px]" />
        <span class="text-[15px] leading-[20px] text-black">.com.br</span>
      </RouterLink>

      <div class="mt-[23px] w-full max-w-[401px] rounded-lg border-[1.5px] border-[#dbdfdf] bg-white p-8">
        <h1 class="text-[22px] text-[#14191f]">Faça login ou crie uma conta</h1>

        <form class="mt-6" @submit.prevent>
          <label for="login-identifier" class="block text-[16px] font-bold text-[#14191f]">
            Digite um número de celular ou e-mail
          </label>
          <input
            id="login-identifier"
            type="text"
            class="mt-2 h-10 w-full rounded-[3px] border border-[#7d8181] px-3 text-[15px] shadow-[inset_3px_4px_4.2px_0px_rgba(0,0,0,0.12)] outline-none focus:border-[#265594]"
          />

          <button
            type="submit"
            class="mt-6 h-10 w-full rounded-full bg-[#fcd533] text-[16px] text-[#14191f] transition hover:bg-[#f7c910]"
          >
            Continuar
          </button>
        </form>

        <p class="mt-6 text-[15px] leading-[20px] text-[#14191f]">
          Ao continuar, você concorda com as
          <a href="#" class="text-[#265594] underline">Condições de Uso</a>
          e a
          <a href="#" class="text-[#265594] underline">Notificação de privacidade</a>
          da Amazon.
        </p>

        <a href="#" class="mt-4 block text-[15px] leading-[20px] text-[#265594] underline">Precisa de ajuda?</a>
      </div>
    </div>

    <div class="mt-16 border-t border-[#e7e7e7] px-4 py-8">
      <nav class="flex flex-wrap justify-center gap-6 text-[14px] text-[#265594] underline">
        <a href="#">Condições de uso</a>
        <a href="#">Notificação de privacidade</a>
        <a href="#">Ajuda</a>
        <a href="#">Aviso de cookies</a>
        <a href="#">Anúncios baseados em interesses</a>
      </nav>
      <p class="mt-4 text-center text-[14px] text-[#2d2d2d]">© 1996-2026, Amazon.com, Inc. ou suas afiliadas</p>
    </div>
  </main>
</template>
