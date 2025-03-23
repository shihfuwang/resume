<script setup lang="ts">
import Title from '@/components/Title.vue'

const props = defineProps<{
  title: string,
  links: { name: string; url: string }[],
  imgSrc: string,
  textFirst: boolean ,
}>()
</script>

<template>
  <div class="flex flex-col my-8">
    <template v-if="props.textFirst">
      <div
        class="
          flex flex-col gap-x-6
          md:flex-row
        "
      >
        <div
          class="
            w-full text-left
            md:w-1/2
          "
        >
          <Title :title="props.title" :size="40" />
          <ul
            class="
              text-green-600 space-y-1 mt-2 text-[16px]
               md:text-[20px]
              "
            >
            <li v-for="(link, index) in props.links" :key="index">
              <a :href="link.url" target="_blank" class="hover:underline">
                {{ link.name }}
              </a>
            </li>
          </ul>
        </div>
        <div
          class="
            w-full text-left my-5
            md:w-2/3 md:my-0
          "
        >
          <img :src="props.imgSrc" />
        </div>
      </div>
    </template>

    <template v-else>
      <div
        class="
          flex flex-col gap-x-6
          md:flex-row
        "
      >
        <div
          class="
            w-full text-left
            md:w-2/3
          "
        >
          <img :src="props.imgSrc"/>
        </div>
        <div
          class="
            w-full text-left
            md:w-1/2
          "
        >
          <Title
            :title="props.title"
            :size="40"
            class="
              my-5
              md:my-0
            "
          />
          <ul
            class="
              text-green-600 space-y-1 mt-2
              text-[16px]
              md:text-[20px]
            "
          >
            <li v-for="(link, index) in props.links" :key="index">
              <a :href="link.url" target="_blank" class="hover:underline">
                {{ link.name }}
              </a>
            </li>
          </ul>
        </div>
      </div>
    </template>
  </div>
</template>