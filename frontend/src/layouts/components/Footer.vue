<template>
  <div class="h-100 d-flex flex-wrap align-center justify-space-between">
    <!-- 👉 Footer: left content -->
    <span class="d-flex align-center">
      &copy;
      {{ new Date().getFullYear() }}
      Made With
      <VIcon
        icon="bx-heart"
        color="error"
        size="1.25rem"
        class="mx-1"
      />
      By <a
        href="javascript:void(0)"
        class="text-primary ms-1"
      >Halliwell Inc.</a>
    </span>
    <span class="d-flex align-center">
      Open Beta
    </span>
  </div>
</template>
