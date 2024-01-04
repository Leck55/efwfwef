<script setup>
import logo from '@images/logo.svg?raw'

</script>

<template>
  <div class="auth-wrapper d-flex align-center justify-center pa-4">
    <VCard
      class="auth-card pa-4 pt-7"
      max-width="448"
    >
      <VCardItem class="justify-center">
        <template #prepend>
          <div class="d-flex">
            <div
              class="d-flex text-primary"
              v-html="logo"
            />
          </div>
        </template>

        <VCardTitle class="text-2xl font-weight-bold">
          WeatherSpace
        </VCardTitle>
      </VCardItem>

      <VCardText class="pt-2">
        <h5 class="text-h5 mb-1">
          WeatherSpace Privacy policy
        </h5>
        <VCol cols="12">
          <span class="text-body-1">
            1. You do not talk about Fight Club……
          </span>
        </VCol>
        <VCol cols="12">
          <span class="text-body-1">
            2. You do NOT talk about Fight Club.
          </span>
        </VCol>
        <VCol cols="12">
          <span class="text-body-1">
            3. If someone says "Stop" or goes limp, taps out, the fight is over.
          </span>
        </VCol>
        <VCol cols="12">
          <span class="text-body-1">
            4. Only two guys to a fight.
          </span>
        </VCol>
        <VCol cols="12">
          <span class="text-body-1">
            5. One fight at a time.
          </span>
        </VCol>
        <VCol cols="12">
          <span class="text-body-1">
            6. No shirts, no shoes.
          </span>
        </VCol>
        <VCol cols="12">
          <span class="text-body-1">
            7. Fights will go on as long as they have to
          </span>
        </VCol>
        <VCol cols="12">
          <span class="text-body-1">
            8. If this is your first time at Fight Club, you have to fight.
          </span>
        </VCol>
        <VCol cols="12" class="text-center text-base">
          <RouterLink 
            class="text-primary ms-2" 
            to="/register"
          >
            Back to registration!
          </RouterLink>
        </VCol>
      </VCardText>
    </VCard>
  </div>
</template>

<style lang="scss">
@use "@core/scss/template/pages/page-auth.scss";
</style>
