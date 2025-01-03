<template>
  <div class="border-2 border-red-500 rounded-md bg-black p-1 px-2 flex items-center gap-3 ">
    <div :class="{'active-theme' : !themeIsDark}" class="cursor-pointer" @click="changeAppTheme(false)">
      <img src="~/assets/icon/sun.png" alt="Main" width="16" height="16"/>
    </div>
    <div :class="{'active-theme' : themeIsDark}" class="cursor-pointer" @click="changeAppTheme(true)">
      <img src="~/assets/icon/moon.svg"  alt="Main" width="16" height="16"/>
    </div>
  </div>
</template>

<script setup>
const themeIsDark = ref(true);

const changeAppTheme = (value) => {
  themeIsDark.value = value;
  if (!value) {
    // Apply dark mode if true
    document.documentElement.classList.add('dark');
  } else {
    // Remove dark mode if false
    document.documentElement.classList.remove('dark');
  }

  // Save the theme preference to localStorage
  localStorage.setItem('darkMode', (!value).toString());
};

onMounted(() => {
  const isDarkMode = localStorage.getItem('darkMode') === 'true';
  if (isDarkMode) {
    document.documentElement.classList.add('dark');
    themeIsDark.value = false;
  } else {
    document.documentElement.classList.remove('dark');
    themeIsDark.value = true;
  }
});

</script>

<style scoped>
.active-theme{
  background-color: red;
  border-radius: 5px;
  padding: 5px;
}
</style>