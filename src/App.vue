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
      <div class="flex grid grid-cols-4 gap-[27px] mt-[35px]">
        <div
          class="w-[280px] h-[459px] border"
          v-for="pizza in pizzas"
          :key="pizza.id"
        >
          <img
            src="../public/vue-pizza.png"
            :alt="pizza.name"
            class="w-[259px] h-[260px] m-auto"
          />
          <h3 class="text-center mt-[11px]">{{ pizza.name }}</h3>
          <div
            class="w-[280px] h-[85px] flex flex-col mt-[22px] bg-[#F3F3F3] rounded-[10px]"
          >
            <div class="w-[265px] m-auto flex justify-between">
              <button>тонкое</button>
              <button>традиционное</button>
            </div>
            <div class="w-[265px] m-auto flex justify-between">
              <button class="gap-4" v-for="size in pizza.sizes" :key="size">
                {{ size }} см.
              </button>
            </div>
          </div>
          <div class="flex justify-between mt-[17px]">
            <p>от {{ pizza.price }} ₽</p>
            <button class="flex">
              <span>+</span>
              <span>Добавить </span>
              <span>2</span>
            </button>
          </div>
        </div>
      </div>
    </main>
    <footer></footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      pizzas: [],
    };
  },
  mounted() {
    fetch("http://localhost:5000/pizzas")
      .then((response) => response.json())
      .then((data) => {
        this.pizzas = data;
      })
      .catch((error) => {
        console.error("Ошибка загрузки данных:", error);
      });
  },
};
</script>

<style scoped></style>
