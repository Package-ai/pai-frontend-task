<template>
  <div class="bg-zinc-500 w-screen h-screen p-5">
    <div
      class="bg-white border border-gray-300 rounded-md p-3 max-w-[1200px] m-auto h-full !font-sans flex flex-col gap-y-2 overflow-hidden"
    >
      <ChatHeader class="flex-shrink-0" />
      <div class="flex-grow overflow-y-auto bg-stone-100 rounded p-2 space-y-2">
        <ChatMessage v-for="item in items" :key="item.id" :item="item" />
      </div>
    </div>
  </div>
</template>

<script setup>
import ChatHeader from './components/ChatHeader.vue'
import ChatMessage from './components/ChatMessage.vue'
import items from './assets/msgs.json'
</script>
