<template>
  <div class="w-[1340px] m-auto border border-red-500">
    <header
      class="w-[90%] h-[137px] flex justify-between items-center border border-green-500 m-auto"
    >
      <div class="flex">
        <div><img src="../public/logo.png" alt="img" /></div>
        <div>
          <h2>REACT PIZZA</h2>
          <p>самая вкусная пицца во вселенной</p>
        </div>
      </div>
      <div class="flex items-center gap-4">
        <div class="text-lg font-bold text-gray-700">520 ₽</div>
        <button
          class="flex items-center gap-2 bg-orange-500 text-white px-4 py-2 rounded"
        >
          <span class="material-icons">shopping_cart</span>
          <span>3</span>
        </button>
      </div>
    </header>
    <nav
      class="w-[90%] h-[46px] flex justify-between items-center m-auto mt-[40px] border border-blue-500 bg-white p-4 shadow"
    >
      <ul class="flex gap-4">
        <li><button class="px-4 py-2 rounded bg-gray-200">Все</button></li>
        <li>
          <button class="px-4 py-2 rounded hover:bg-gray-100">Мясные</button>
        </li>
        <li>
          <button class="px-4 py-2 rounded hover:bg-gray-100">
            Вегетарианская
          </button>
        </li>
        <li>
          <button class="px-4 py-2 rounded hover:bg-gray-100">Гриль</button>
        </li>
        <li>
          <button class="px-4 py-2 rounded hover:bg-gray-100">Острые</button>
        </li>
        <li>
          <button class="px-4 py-2 rounded hover:bg-gray-100">Закрытые</button>
        </li>
      </ul>
      <div>
        <span>Сортировка по:</span>
        <select class="ml-2 border rounded px-2 py-1">
          <option>популярности</option>
          <option>по цене</option>
          <option>по алфавиту</option>
        </select>
      </div>
    </nav>
    <main class="w-[90%] m-auto mt-[32px] border border-yellow-500">
      <h2>Все пиццы</h2>
      <div class="flex justify-between mt-[35px]">
        <div class="w-[280px] h-[459px] border"></div>
        <div class="w-[280px] h-[459px] border"></div>
        <div class="w-[280px] h-[459px] border"></div>
        <div class="w-[280px] h-[459px] border"></div>
      </div>
      <div class="flex justify-between mt-[65px]">
        <div class="w-[280px] h-[459px] border"></div>
        <div class="w-[280px] h-[459px] border"></div>
        <div class="w-[280px] h-[459px] border"></div>
        <div class="w-[280px] h-[459px] border"></div>
      </div>
      <div class="flex justify-between mt-[65px]">
        <div class="w-[280px] h-[459px] border"></div>
        <div class="w-[280px] h-[459px] border"></div>
        <div class="w-[280px] h-[459px] border"></div>
        <div class="w-[280px] h-[459px] border"></div>
      </div>

    </main>
    <footer></footer>
  </div>
</template>

<script setup></script>
<style scoped></style>
