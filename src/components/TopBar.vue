<script setup lang="ts">
import {Bell , Menu , Moon, Search , Sun} from "lucide-vue-next"

defineProps<{
darkMode :boolean
search:string
}>()

const emit = defineEmits <{
    "update:search" : [value :string]
    toggleThem :[]
    openSidebar :[]
}>()
</script>

<template>
<header class="topbar">
    <button
    class="mobile-menu"
     @click="emit('openSidebar')"
    >
    <Menu :size="22"/>
</button>

<div class="page-title">
    <span>Overview</span>

    <h1>
        Hello
        <span></span>
    </h1>
</div>
<div class="top-action">

    <label class="search-box">
        <search :size="18"></search>
 
    <input type="text"
    :value="search"
    placeholder="Search assets....."
    @input="
    emit(
        'update:search',
         ($event.target as HTMLInputElement).value
    )
    "
    />

       <kbd>⌘ K</kbd>
          </label>

  <button
  class="icon-btn"
  @click="emit('toggleThem')"
  >
  <Sun
  v-if="!darkMode"
  :size="19"
  />

  <Moon
  v-else
  :size="19"
  />
</button>

<button class="icon-btn notification">
    <Bell
    :size="19"/>
    <i></i>
</button>

<button class="user-mini">
    ZS
</button>

</div>
</header>
</template>