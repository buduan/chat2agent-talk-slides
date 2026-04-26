<template>
  <div class="h-full w-full flex flex-col items-center justify-center bg-gradient-to-br from-gray-50 to-sky-50 text-center p-4">
    <div class="text-8xl font-black text-sky-100 leading-none -mb-2 select-none">
      Part {{ $frontmatter.part || 1 }}
    </div>
    <div class="text-6xl font-bold text-slate-900 mb-4 leading-tight tracking-tight">
      {{ $frontmatter.partTitle || 'Part Title' }}
    </div>
    <div class="text-2xl font-medium text-sky-500 mb-8">
      {{ $frontmatter.partSubtitle || '' }}
    </div>
    <div v-if="$frontmatter.partDescription" class="text-lg text-slate-600 leading-relaxed max-w-[700px]">
      {{ $frontmatter.partDescription }}
    </div>
  </div>
</template>

<style scoped>
/* Reset for layout */
.slidev-layout {
  margin: 0;
  padding: 0;
}
</style>
