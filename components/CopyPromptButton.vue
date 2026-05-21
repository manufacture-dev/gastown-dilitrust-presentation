<script setup>
async function copyDemoPrompt() {
  const response = await fetch(`${import.meta.env.BASE_URL}prompts/gastown-demo-prompt.txt`)
  if (!response.ok)
    throw new Error(`Prompt fetch failed: ${response.status}`)

  await navigator.clipboard.writeText(await response.text())
}
</script>

<template>
  <button class="app-open-link" type="button" @click="copyDemoPrompt">
    Copy prompt
  </button>
</template>
