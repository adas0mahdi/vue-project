<script setup>
import { ref } from "vue";
import { Dialog, DialogPanel, PopoverGroup } from "@headlessui/vue";
import {
  Bars3Icon,
  XMarkIcon,
  MagnifyingGlassIcon,
  UserIcon,
  ShoppingCartIcon,
} from "@heroicons/vue/24/outline";
const mobileMenuOpen = ref(false);
</script>
<template>
  <header class="relative text-white z-50">
    <nav
      class="mx-auto flex max-w-7xl items-center justify-between p-6 lg:px-8"
      aria-label="Global"
    >
      <div class="flex lg:flex-1">
        <a href="#" class="-m-1.5 p-1.5">
          <span class="sr-only">Your Company</span>
          <img class="h-[70px] w-auto" src="../assets/image/logo.png" alt="" />
        </a>
      </div>
      <div class="flex lg:hidden">
        <button
          type="button"
          class="-m-2.5 inline-flex items-center justify-center rounded-md p-2.5 text-gray-700"
          @click="mobileMenuOpen = true"
        >
          <span class="sr-only">Open main menu</span>
          <Bars3Icon class="h-10 w-10 text-black" aria-hidden="true" />
        </button>
      </div>
      <PopoverGroup class="hidden lg:flex lg:gap-x-12">
        <a href="#" class="text-[12px] leading-6">SIGNATURE CAKES</a>
        <a href="#" class="text-[12px] leading-6">BESPOKE CAKES</a>
        <a href="#" class="text-[12px] leading-6">WEDDING CAKES</a>
        <a href="#" class="text-[12px] leading-6">CAKESICLES</a>
        <a href="#" class="text-[12px] leading-6">CHOCOLATES</a>
        <a href="#" class="text-[12px] leading-6">MASTER CLASSES</a>
      </PopoverGroup>
      <div class="hidden lg:flex lg:flex-1 lg:justify-end gap-6">
        <div class="p-2 backdrop-blur-xl rounded-full">
          <a href=""><MagnifyingGlassIcon class="h-6 w-6" /></a>
        </div>
        <div class="p-2 backdrop-blur-xl rounded-full">
          <a href=""><UserIcon class="h-6 w-6" /></a>
        </div>
        <div class="p-2 backdrop-blur-xl rounded-full">
          <a href=""> <ShoppingCartIcon class="h-6 w-6" /></a>
        </div>
      </div>
    </nav>

    <Dialog
      as="div"
      class="lg:hidden"
      @close="mobileMenuOpen = false"
      :open="mobileMenuOpen"
    >
      <div class="fixed inset-0 z-10" />
      <DialogPanel
        class="fixed inset-y-0 right-0 z-10 w-full overflow-y-auto backdrop-blur-sm px-6 py-6 sm:max-w-sm sm:ring-1 sm:ring-gray-900/10"
      >
        <div class="flex items-center justify-between">
          <a href="#" class="-m-1.5 p-1.5">
            <span class="sr-only">Your Company</span>
            <img
              class="h-[70px] w-auto"
              src="../assets/image/logo.png"
              alt=""
            />
          </a>
          <button
            type="button"
            class="-m-2.5 rounded-md p-2.5 text-gray-700"
            @click="mobileMenuOpen = false"
          >
            <span class="sr-only">Close menu</span>
            <XMarkIcon class="h-8 w-8 text-black" aria-hidden="true" />
          </button>
        </div>
        <div class="mt-6 flow-root">
          <div class="-my-6 divide-y divide-gray-500/10">
            <div class="space-y-2 py-6">
              <a
                href="#"
                class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 hover:bg-gray-50"
                >SIGNATURE CAKES</a
              >
              <a
                href="#"
                class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 hover:bg-gray-50"
                >BESPOKE CAKES</a
              >
              <a
                href="#"
                class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 hover:bg-gray-50"
                >WEDDING CAKES</a
              >
              <a
                href="#"
                class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 hover:bg-gray-50"
                >CAKESICLES</a
              >
              <a
                href="#"
                class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 hover:bg-gray-50"
                >CHOCOLATES</a
              >
              <a
                href="#"
                class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 hover:bg-gray-50"
                >MASTER CLASSES</a
              >
            </div>
            <div class="py-6">
              <div class="flex gap-4">
                <MagnifyingGlassIcon
                  class="h-10 w-10 hover:bg-gray-50 hover:rounded-full hover:m-2 p-2"
                />
                <UserIcon
                  class="h-10 w-10 hover:bg-gray-50 hover:rounded-full hover:m-2 p-2"
                />
                <ShoppingCartIcon
                  class="h-10 w-10 hover:bg-gray-50 hover:rounded-full hover:m-2 p-2"
                />
              </div>
            </div>
          </div>
        </div>
      </DialogPanel>
    </Dialog>
  </header>
</template>
