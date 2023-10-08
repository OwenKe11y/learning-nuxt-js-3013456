<template>
  <div
    class="relative flex items-top justify-center min-h-screen bg-gray-100 sm:items-center sm:pt-8 sm:pb-8"
  >
    <link
      href="https://cdn.jsdelivr.net/npm/tailwindcss@2.1.2/dist/tailwind.min.css"
      rel="stylesheet"
    />

    <div>
      <div class="flex justify-center pt-8 sm:pt-0">
        <a href="https://nuxtjs.org" target="_blank">
          <NuxtLogo />
        </a>
      </div>
      <div class="mt-6 bg-white overflow-hidden shadow sm:rounded-lg p-6">
        <Header />
      </div>
      <div class="mt-6 bg-white overflow-hidden shadow sm:rounded-lg p-6">
        <MainText />
      </div>
      <div class="mt-6 bg-white overflow-hidden shadow sm:rounded-lg p-6">
        <img
          src="~/assets/img/shinto-fnf.gif"
          alt="Gettin' freaky on a friday night,
        yeah."
        />
      </div>
    </div>
  </div>
</template>
