<script setup>
import { useI18n } from 'vue-i18n'

const { locale, t } = useI18n()

async function copyDemoPrompt() {
  const lang = locale.value?.startsWith('fr') ? 'fr' : 'en'
  const response = await fetch(`${import.meta.env.BASE_URL}prompts/gastown-demo-prompt.${lang}.txt`)
  if (!response.ok)
    throw new Error(`Prompt fetch failed: ${response.status}`)

  await navigator.clipboard.writeText(await response.text())
}
</script>

<template>
  <button class="app-open-link" type="button" :aria-label="t('demo.copy_prompt')" @click="copyDemoPrompt">
    {{ t('demo.copy_prompt') }}
  </button>
</template>
