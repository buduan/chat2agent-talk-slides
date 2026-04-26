<template>
  <div class="slidev-layout cover-layout h-full w-full flex flex-col items-center justify-center relative overflow-hidden bg-gradient-to-br from-sky-50 via-sky-100 to-sky-50 font-sans">

    <!-- Animated Background Orbs -->
    <div class="absolute inset-0 overflow-hidden pointer-events-none">
      <div class="bg-orb absolute rounded-full blur-[80px] op-40 w-100 h-100 bg-sky-200 -top-25 -right-25 animate-orb-1" />
      <div class="bg-orb absolute rounded-full blur-[80px] op-40 w-87.5 h-87.5 bg-sky-100 -bottom-20 -left-20 animate-orb-2" />
      <div class="bg-orb absolute rounded-full blur-[80px] op-30 w-70 h-70 bg-sky-300 top-1/2 left-30% -translate-x-1/2 -translate-y-1/2 animate-orb-3" />
    </div>

    <!-- Main Content -->
    <div class="relative z-10 text-center px-8 max-w-6xl mx-auto w-full flex flex-col items-center justify-center">
      <slot />
    </div>

  </div>
</template>

<script setup lang="ts">
</script>

<style scoped>
/* Override global heading positioning for cover */
.cover-layout :deep(h1),
.cover-layout :deep(h2),
.cover-layout :deep(h3) {
  position: static;
  transform: none;
  text-align: center;
}

/* Gradient text for h1 */
.cover-layout :deep(h1) {
  font-size: 4rem;
  line-height: 1.2;
  letter-spacing: -0.02em;
  font-weight: bold;
}

.cover-layout :deep(h2) {
  font-size: 2rem;
  font-weight: 700;
  color: #475569;
  margin-top: 1.5rem;
}

/* Orb float animation */
@keyframes float-orb {
  0%, 100% { transform: translate(0, 0) scale(1); }
  50%       { transform: translate(-20px, -20px) scale(1.1); }
}

.animate-orb-1 { animation: float-orb 8s ease-in-out 0s infinite; }
.animate-orb-2 { animation: float-orb 8s ease-in-out 2s infinite; }
.animate-orb-3 { animation: float-orb 8s ease-in-out 4s infinite; }

@media (max-width: 768px) {
  .cover-layout :deep(h1) { font-size: 2.5rem; }
  .cover-layout :deep(h2) { font-size: 1.5rem; }
  .animate-orb-1, .animate-orb-2, .animate-orb-3 { width: 200px; height: 200px; }
}
</style>
