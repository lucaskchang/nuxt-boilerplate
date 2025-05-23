<template>
  <div class="flex h-screen flex-col items-center justify-center p-4">
    <div class="mx-auto flex w-full flex-col text-center md:w-2/3">
      <p
        class="text-6xl font-bold md:text-9xl"
        :class="{ 'font-sans': $colorMode.value === 'dark', 'patrick': $colorMode.value !== 'dark' }"
      >
        All-in-one<br>
        <span
          :class="{ 'bg-linear-to-r from-teal-300 via-sky-600 to-cyan-300 bg-clip-text font-sans text-transparent': $colorMode.value === 'dark', 'patrick text-cyan-500': $colorMode.value !== 'dark' }"
        >
          Nuxt Boilerplate
        </span>
      </p>
      <p
        :class="{ 'inter mt-4 md:text-lg': $colorMode.value === 'dark', 'nunito mt-6 md:text-lg': $colorMode.value !== 'dark' }"
      >
        Nuxt Boilerplate is an
        <a
          href="https://github.com/lucaskchang/nuxt-boilerplate"
          target="_blank"
          rel="noopener noreferrer"
          class="font-bold text-cyan-500 hover:text-cyan-600"
        >
          open source template
        </a>
        that includes everything you need to create a modern web application with
        <a
          href="https://nuxt.com/"
          target="_blank"
          rel="noopener noreferrer"
          class="font-bold text-cyan-500 hover:text-cyan-600"
        >
          Nuxt.js</a>,
        <a
          href="https://tailwindcss.com/"
          target="_blank"
          rel="noopener noreferrer"
          class="font-bold text-cyan-500 hover:text-cyan-600"
        >
          TailwindCSS</a>,
        <a
          href="https://pinia.vuejs.org/"
          target="_blank"
          rel="noopener noreferrer"
          class="font-bold text-cyan-500 hover:text-cyan-600"
        >
          Pinia</a>,
        and
        <a
          href="https://vueuse.org/"
          target="_blank"
          rel="noopener noreferrer"
          class="font-bold text-cyan-500 hover:text-cyan-600"
        >
          VueUse</a>.
      </p>
      <div class="mt-4 flex flex-row justify-center space-x-4">
        <UButton
          size="lg"
          label="Try it yourself here"
          icon="i-heroicons-arrow-right"
          to="https://github.com/lucaskchang/nuxt-boilerplate"
          trailing
        />
      </div>
    </div>
    <div class="sticky top-full mx-auto flex flex-col">
      <p
        class="md:text-lg"
        :class="{ inter: $colorMode.value === 'dark', nunito: $colorMode.value !== 'dark' }"
      >
        Created by
        <a
          href="https://www.lucaskchang.com/"
          target="_blank"
          rel="noopener noreferrer"
          class="font-semibold text-cyan-500 hover:text-cyan-600"
          :class="{ 'font-sans': $colorMode.value === 'dark' }"
        >
          Lucas Chang
        </a>
      </p>
    </div>
    <div
      v-if="$colorMode.value === 'dark'"
      class="glow fixed right-8 top-8 size-1"
    />
    <div
      v-else
      class="fixed -right-8 -top-8"
    >
      <svg
        width="159"
        height="125"
        viewBox="0 0 159 125"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          d="M141.595 86.2654C142.406 85.1642 143.633 83.2905 145.043 80.9047C146.425 78.4997 147.902 75.5343 149.139 72.2503C150.385 68.9759 151.36 65.3925 151.843 61.8573C152.346 58.3318 152.375 54.8837 152.036 51.9087C151.302 45.0316 148.607 38.4346 144.242 33.0642C139.905 27.6649 134.081 23.4053 127.628 20.5849C121.176 17.7355 114.125 16.4219 106.978 16.5185C99.8397 16.6055 92.6826 18.0446 85.8634 20.5077C83.7191 21.2514 80.918 22.4877 78.5709 23.386C77.3925 23.8206 76.3301 24.1781 75.4994 24.3037C74.6591 24.4196 74.0506 24.294 73.8091 23.811C73.3068 22.8065 74.0312 21.2996 75.934 19.619C77.8175 17.9287 80.8891 16.1033 84.9168 14.6448C94.6626 11.1869 105.278 9.67043 115.651 11.1386C120.848 11.805 125.899 13.3408 130.681 15.4271C135.413 17.6003 139.924 20.3338 143.865 23.7917C149.67 28.766 154.277 35.392 156.653 42.81C159.087 50.2184 159.281 58.2352 157.774 65.7305C156.277 73.2645 153.196 80.3252 149.197 86.7194C145.179 93.1136 140.233 98.8606 134.592 103.845C132.052 106.076 129.367 108.152 126.547 110.026C125.841 110.5 125.136 110.963 124.402 111.398C123.678 111.842 122.963 112.296 122.21 112.683L117.767 115.078C111.72 118.034 105.374 120.342 98.8545 121.984C92.3444 123.665 85.6316 124.505 78.909 124.708L76.3879 124.785C75.5476 124.804 74.7074 124.737 73.8671 124.717L71.346 124.621C70.5057 124.602 69.6653 124.563 68.825 124.457L63.7927 123.925L58.8088 123.037C52.5981 121.733 46.5034 119.82 40.6984 117.145C37.8587 115.686 34.9707 114.305 32.3145 112.499C29.5714 110.857 26.9924 108.886 24.5391 106.81C14.7739 98.3776 7.57792 87.1927 3.62743 74.9742C0.198523 64.4363 -0.699603 53.0194 1.3674 42.0566C1.86966 39.3135 2.623 36.6186 3.48264 33.9721C4.42921 31.3449 5.4433 28.737 6.76657 26.274C7.36542 25.0087 8.12858 23.8399 8.8047 22.6229L9.96372 20.836L11.2098 19.1167C12.9194 16.8662 14.8414 14.7896 16.9084 12.8964C20.7623 9.313 25.9011 5.40115 31.3776 3.23755C33.6185 2.32962 36.7189 1.32507 39.9546 0.803494C43.1807 0.272255 46.5131 0.252975 48.9568 0.600695C51.0721 0.890462 53.226 1.412 55.2447 2.01086C59.91 3.43071 62.3923 5.51706 63.194 6.74374C64.0343 7.99939 63.2905 8.45335 61.378 8.54028C60.5473 8.60789 60.6923 9.53513 58.8668 8.77208C58.7895 8.7431 58.6446 8.68515 58.5673 8.65618C57.1088 8.22153 55.7374 7.75787 54.3272 7.41981C52.9363 7.04312 51.526 6.73409 50.0965 6.51193C48.667 6.25114 47.1988 6.16417 45.7113 6.10622C44.2238 6.10622 42.7171 6.17381 41.22 6.44425C33.8696 7.69991 26.8764 11.4476 21.2742 16.4992C19.864 17.7645 18.5506 19.1264 17.3432 20.5752C16.1359 22.0144 15.0153 23.5309 14.0591 25.1343C12.0983 28.3797 10.495 31.8859 9.30698 35.5079C6.90192 42.7714 6.16778 50.5757 6.82458 58.2546C7.49104 65.9334 9.55799 73.506 12.8034 80.5184C14.8028 84.8166 17.2175 88.9312 20.0766 92.6982C22.9259 96.4748 26.152 99.9714 29.7838 102.975L31.1458 104.105L32.556 105.158C33.4736 105.892 34.5071 106.481 35.4923 107.138C36.4969 107.766 37.4626 108.442 38.4865 109.031L41.6256 110.683L43.2001 111.504L44.8324 112.2L48.097 113.581C49.2078 113.986 50.3475 114.334 51.468 114.711C52.598 115.078 53.7088 115.483 54.8679 115.725L58.6544 116.614C59.9197 116.884 61.2236 117.019 62.4986 117.232L64.4207 117.541C65.0678 117.647 65.715 117.676 66.3718 117.753C67.6758 117.889 68.9698 118.043 70.2738 118.236L70.187 118.227C75.6829 118.468 81.1885 118.275 86.6458 117.609C91.794 116.903 96.9904 115.957 102.003 114.295L103.896 113.726C104.524 113.523 105.133 113.272 105.751 113.04L109.45 111.649L113.043 110.007C113.642 109.727 114.251 109.476 114.83 109.176L116.559 108.239C125.871 103.487 133.762 96.5135 139.895 88.7574C140.397 88.1006 140.948 87.2023 141.595 86.2654Z"
          fill="rgba(56,191,248,0.9)"
        />
      </svg>
    </div>
    <ColorMode />
  </div>
</template>

<style>
.patrick {
  font-family: 'Patrick Hand', cursive;
}

.inter {
  font-family: 'Inter', sans-serif;
}

.nunito {
  font-family: 'Nunito', sans-serif;
}

.glow {
  -webkit-box-shadow:0px 0px 105px 112px rgba(56,191,248,0.9);
  -moz-box-shadow: 0px 0px 105px 112px rgba(56,191,248,0.9);
  box-shadow: 0px 0px 105px 112px rgba(56,191,248,0.9);
}
</style>
