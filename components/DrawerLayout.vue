<template>
  <div class="drawer lg:drawer-open">
    <input id="my-drawer-2" type="checkbox" class="drawer-toggle" />
    <div class="drawer-content flex flex-col items-center">
      <nav class="w-full navbar bg-base-100 shadow-sm sticky top-0 z-10">
        <div class="flex-none lg:hidden flex-none">
          <label
            for="my-drawer-2"
            aria-label="open sidebar"
            class="btn btn-square btn-ghost"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              class="inline-block w-6 h-6 stroke-current"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M4 6h16M4 12h16M4 18h16"
              ></path>
            </svg>
          </label>
        </div>
        <slot name="header"> </slot>
      </nav>
      <slot name="body"> </slot>
    </div>
    <div class="drawer-side z-10">
      <label
        for="my-drawer-2"
        aria-label="close sidebar"
        class="drawer-overlay"
      ></label>
      <ul class="menu p-4 w-60 min-h-full bg-base-100 text-base-content">
        <slot name="bar"> </slot>
      </ul>
    </div>
  </div>
</template>
