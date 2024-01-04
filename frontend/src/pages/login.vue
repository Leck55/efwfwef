<script setup>
import AuthProvider from '@/views/pages/authentication/AuthProvider.vue'
import logo from '@images/logo.svg?raw'

const form = ref({
  email: '',
  password: '',
  remember: false,
})

const isPasswordVisible = ref(false)
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
          Welcome to WeatherSpace! 👋🏻
        </h5>
        <p class="mb-0">
          Experience our open beta!
        </p>
      </VCardText>

      <VCardText>
        <VForm @submit.prevent="$router.push('/')">
          <VRow>
            <!-- email -->
            <VCol cols="12">
              <VTextField
                v-model="form.email"
                autofocus
                placeholder="me@mail.com"
                label="Email"
                type="email"
              />
            </VCol>

            <!-- password -->
            <VCol cols="12">
              <VTextField
                v-model="form.password"
                label="Password"
                placeholder="············"
                :type="isPasswordVisible ? 'text' : 'password'"
                :append-inner-icon="isPasswordVisible ? 'bx-hide' : 'bx-show'"
                @click:append-inner="isPasswordVisible = !isPasswordVisible"
              />
            </VCol>

            <VCol cols="12">               
              <VBtn
                block
                type="submit"
                cols="12"
              >
                Login
              </VBtn>
            </VCol>
            <!-- create account -->
            <VCol
              cols="12"
              class="text-center text-base"
            >
              <span>Join us!</span>
              <RouterLink
                class="text-primary ms-2"
                to="/register"
              >
                Create an account
              </RouterLink>
            </VCol>
          </VRow>
        </VForm>
      </VCardText>
    </VCard>
  </div>
</template>

<style lang="scss">
@use "@core/scss/template/pages/page-auth.scss";
</style>
