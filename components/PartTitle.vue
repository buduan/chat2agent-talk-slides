<template>
  <div class="part-title-wrapper">
    <!-- Background decorative elements -->
    <div class="part-title-bg">
      <div class="circle circle-1"></div>
      <div class="circle circle-2"></div>
      <div class="circle circle-3"></div>
    </div>

    <!-- Main content -->
    <div class="part-title-content">
      <!-- Part number with animation -->
      <div class="part-number">
        <div class="part-number-text">Part {{ partNumber }}</div>
      </div>

      <!-- Part title with stagger animation -->
      <h1 class="part-title">
        <span
          v-for="(word, index) in titleWords"
          :key="index"
          class="title-word"
          :style="{ animationDelay: `${index * 100 + 300}ms` }"
        >
          {{ word }}
        </span>
      </h1>

      <!-- Subtitle with fade-in -->
      <div class="part-subtitle" :style="{ animationDelay: '600ms' }">
        {{ subtitle }}
      </div>

      <!-- Optional description -->
      <div v-if="description" class="part-description" :style="{ animationDelay: '800ms' }">
        {{ description }}
      </div>
    </div>

    <!-- Progress indicator -->
    <div class="part-progress">
      <div class="progress-bar">
        <div
          class="progress-fill"
          :style="{ width: `${(partNumber / totalParts) * 100}%` }"
        ></div>
      </div>
      <div class="progress-text">{{ partNumber }} / {{ totalParts }}</div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { computed } from 'vue'

interface Props {
  partNumber: number
  title: string
  subtitle: string
  description?: string
  totalParts?: number
}

const props = withDefaults(defineProps<Props>(), {
  totalParts: 4,
  description: ''
})

const titleWords = computed(() => {
  return props.title.split(' ')
})
</script>

<style scoped>
.part-title-wrapper {
  position: relative;
  width: 100%;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  overflow: hidden;
  background: linear-gradient(135deg, #fafafa 0%, #f0f9ff 100%);
}

/* Background decorative circles */
.part-title-bg {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  pointer-events: none;
  z-index: 0;
}

.circle {
  position: absolute;
  border-radius: 50%;
  background: linear-gradient(135deg, rgba(14, 165, 233, 0.1) 0%, rgba(56, 189, 248, 0.05) 100%);
  animation: float 20s ease-in-out infinite;
}

.circle-1 {
  width: 400px;
  height: 400px;
  top: -100px;
  right: -100px;
  animation-delay: 0s;
}

.circle-2 {
  width: 300px;
  height: 300px;
  bottom: -50px;
  left: -50px;
  animation-delay: -7s;
}

.circle-3 {
  width: 200px;
  height: 200px;
  top: 50%;
  left: 10%;
  animation-delay: -14s;
}

@keyframes float {
  0%, 100% {
    transform: translate(0, 0) scale(1);
  }
  33% {
    transform: translate(30px, -30px) scale(1.05);
  }
  66% {
    transform: translate(-20px, 20px) scale(0.95);
  }
}

/* Main content */
.part-title-content {
  position: relative;
  z-index: 1;
  text-align: center;
  max-width: 900px;
  padding: 1rem;
}

/* Part number badge */
.part-number {
  margin-bottom: 2rem;
  animation: fadeInScale 600ms ease-out forwards;
  opacity: 0;
}

.part-number-text {
  display: inline-block;
  padding: 0.75rem 2rem;
  background: linear-gradient(135deg, #0ea5e9 0%, #38bdf8 100%);
  color: white;
  font-size: 1rem;
  font-weight: 600;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  border-radius: 2rem;
  box-shadow: 0 4px 12px rgba(14, 165, 233, 0.3);
}

@keyframes fadeInScale {
  from {
    opacity: 0;
    transform: scale(0.8);
  }
  to {
    opacity: 1;
    transform: scale(1);
  }
}

/* Part title */
.part-title {
  font-size: 4rem;
  font-weight: 700;
  line-height: 1.2;
  margin: 2rem 0;
  color: #0f172a;
  letter-spacing: -0.02em;
}

.title-word {
  display: inline-block;
  opacity: 0;
  animation: slideUp 500ms ease-out forwards;
  margin: 0 0.3rem;
}

.title-word:first-child {
  margin-left: 0;
}

@keyframes slideUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Subtitle */
.part-subtitle {
  font-size: 2rem;
  font-weight: 500;
  color: #0ea5e9;
  margin-top: 1.5rem;
  opacity: 0;
  animation: fadeIn 600ms ease-out forwards;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

/* Optional description */
.part-description {
  margin-top: 2rem;
  font-size: 1.25rem;
  color: #475569;
  max-width: 700px;
  margin-left: auto;
  margin-right: auto;
  line-height: 1.7;
  opacity: 0;
  animation: fadeIn 600ms ease-out forwards;
}

/* Progress indicator */
.part-progress {
  position: absolute;
  bottom: 3rem;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.75rem;
  z-index: 1;
  opacity: 0;
  animation: fadeIn 600ms ease-out 1000ms forwards;
}

.progress-bar {
  width: 200px;
  height: 4px;
  background: rgba(14, 165, 233, 0.2);
  border-radius: 2px;
  overflow: hidden;
}

.progress-fill {
  height: 100%;
  background: linear-gradient(90deg, #0ea5e9 0%, #38bdf8 100%);
  border-radius: 2px;
  transition: width 0.6s ease-out;
  animation: progressGlow 2s ease-in-out infinite;
}

@keyframes progressGlow {
  0%, 100% {
    box-shadow: 0 0 5px rgba(14, 165, 233, 0.5);
  }
  50% {
    box-shadow: 0 0 15px rgba(14, 165, 233, 0.8);
  }
}

.progress-text {
  font-size: 0.875rem;
  font-weight: 500;
  color: #94a3b8;
  letter-spacing: 0.05em;
}

/* Responsive design */
@media (max-width: 768px) {
  .part-title {
    font-size: 2.5rem;
  }

  .part-subtitle {
    font-size: 1.5rem;
  }

  .part-description {
    font-size: 1rem;
  }

  .circle-1 {
    width: 250px;
    height: 250px;
  }

  .circle-2 {
    width: 200px;
    height: 200px;
  }

  .circle-3 {
    width: 150px;
    height: 150px;
  }
}
</style>
