<template>
  <div class="h-64 bg-gray-100 text-center text-sm pt-8">
    <p>
      {{ t('footer.underlicense') }}
      <a
          href="https://opensource.org/licenses/MIT"
          class="text-decoration-none text-teal-600"
          target="_blank">{{ $t('footer.mitlicense') }}</a>
    </p>
    <p>
      &copy; 2022 - {{ year }} Tien Do Nam {{ t('footer.andcontributor') }}
    </p>

    <!-- Links -->
    <div class="flex flex-wrap justify-center mt-8">
      <TextButton href="https://github.com/localsend/localsend" target="_blank" icon="fa6-brands:github">
        {{ t('footer.github') }}
      </TextButton>

      <TextButton href="https://discord.gg/GSRWmQNP87" target="_blank" icon="fa6-brands:discord" class="ml-2">
        {{ t('footer.discord') }}
      </TextButton>

      <NuxtLink to="/privacy" class="ml-2">
        <TextButton icon="material-symbols:shield-lock">
          {{ t('footer.privacy') }}
        </TextButton>
      </NuxtLink>

      <NuxtLink to="/terms" class="ml-2">
        <TextButton icon="material-symbols:gavel">
          {{ t('footer.terms') }}
        </TextButton>
      </NuxtLink>

      <NuxtLink to="/imprint" class="ml-2">
        <TextButton icon="material-symbols:info">
          {{ t('footer.imprint') }}
        </TextButton>
      </NuxtLink>

      <NuxtLink to="/contact" class="ml-2">
        <TextButton icon="material-symbols:chat-bubble">
          {{ t('footer.contact') }}
        </TextButton>
      </NuxtLink>
    </div>
  </div>
</template>

<script setup lang="ts">
const year = new Date().getFullYear();

const { t } = useI18n()
const localePath = useLocalePath()

</script>
