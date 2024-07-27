<script setup>
definePageMeta({
  middleware: function () {
    const currentUser = useCookie('current-user')
    const isAuthenticated = useCookie('is-authenticated')

    currentUser.value = ''
    isAuthenticated.value = ''

    return navigateTo('/')
  }
})
</script>

<template>
  <article class="grid">
    <div>
      <hgroup>
        <h1>Logout</h1>
        <p>This is a simple logout page.</p>
      </hgroup>
    </div>
  </article>
</template>

<style lang="scss" scoped></style>
