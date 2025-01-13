<template>
  <div class="w-[1340px] m-auto border border-red-300">
    <header class="w-[95%] border-b-2 border-b-[#F6F6F6] m-auto">
      <div class="w-[90%] h-[137px] flex justify-between items-center m-auto">
        <div class="flex items-center gap-[17px]">
          <div class="w-[38px] h-[38px]">
            <img src="../public/logo.png" alt="img" />
          </div>
          <div>
            <h2 class="text-[24px] text-[#181818] font-extrabold">
              REACT PIZZA
            </h2>
            <p class="text-[16px] text-[#7B7B7B] font-normal">
              самая вкусная пицца во вселенной
            </p>
          </div>
        </div>
        <div class="flex items-center gap-4">
          <button
            class="w-[150px] h-[50px] flex items-center gap-2 bg-[#FE5F1E] text-white px-4 py-2 rounded-[30px]"
          >
            <span class="text-[16px] font-bold">520 ₽</span>
            <span class="w-[16px] h-[16px]"><img src="" alt="img" /></span>
            <span class="text-[16px] font-bold">3</span>
          </button>
        </div>
      </div>
    </header>
    <nav
      class="w-[90%] h-[46px] flex justify-between items-center m-auto mt-[40px]"
    >
      <ul class="flex gap-[10px]">
        <li>
          <button
            class="text-[16px] text-[#2C2C2C] font-bold rounded-[30px] bg-[#F9F9F9] pt-[10px] pr-[25px] pb-[10px] pl-[25px] hover:bg-[#282828] hover:text-white transition duration-400"
          >
            Все
          </button>
        </li>
        <li>
          <button
            class="text-[16px] text-[#2C2C2C] font-bold rounded-[30px] bg-[#F9F9F9] pt-[10px] pr-[25px] pb-[10px] pl-[25px] hover:bg-[#282828] hover:text-white transition duration-400"
          >
            Мясные
          </button>
        </li>
        <li>
          <button
            class="text-[16px] text-[#2C2C2C] font-bold rounded-[30px] bg-[#F9F9F9] pt-[10px] pr-[25px] pb-[10px] pl-[25px] hover:bg-[#282828] hover:text-white transition duration-400"
          >
            Вегетарианская
          </button>
        </li>
        <li>
          <button
            class="text-[16px] text-[#2C2C2C] font-bold rounded-[30px] bg-[#F9F9F9] pt-[10px] pr-[25px] pb-[10px] pl-[25px] hover:bg-[#282828] hover:text-white transition duration-400"
          >
            Гриль
          </button>
        </li>
        <li>
          <button
            class="text-[16px] text-[#2C2C2C] font-bold rounded-[30px] bg-[#F9F9F9] pt-[10px] pr-[25px] pb-[10px] pl-[25px] hover:bg-[#282828] hover:text-white transition duration-400"
          >
            Острые
          </button>
        </li>
        <li>
          <button
            class="text-[16px] text-[#2C2C2C] font-bold rounded-[30px] bg-[#F9F9F9] pt-[10px] pr-[25px] pb-[10px] pl-[25px] hover:bg-[#282828] hover:text-white transition duration-400"
          >
            Закрытые
          </button>
        </li>
      </ul>
      <div>
        <span class="text-[14px] text-[#2C2C2C] font-bold">Сортировка по:</span>
        <select class="text-[14px] text-[#000000] font-normal ml-2">
          <option>популярности</option>
          <option>по цене</option>
          <option>по алфавиту</option>
        </select>
      </div>
    </nav>
    <main class="w-[90%] m-auto mt-[32px]">
      <h2 class="text-[32px] text-[#000000] font-bold">Все пиццы</h2>
      <div class="flex grid grid-cols-4 gap-[27px] mt-[35px]">
        <div
          class="w-[280px] h-[459px] mb-[40px]"
          v-for="pizza in pizzas"
          :key="pizza.id"
        >
          <img
            src="../public/vue-pizza.png"
            :alt="pizza.name"
            class="w-[259px] h-[260px] m-auto"
          />
          <h3
            class="text-[20px] text-[#000000] text-center font-bold mt-[11px]"
          >
            {{ pizza.name }}
          </h3>
          <div
            class="w-[280px] h-[85px] flex flex-col mt-[22px] bg-[#F3F3F3] rounded-[10px]"
          >
            <div class="w-[265px] m-auto flex justify-between">
              <button
                class="w-[131px] h-[32px] text-[14px] text-[#2C2C2C] font-bold hover:bg-white rounded-[5px] transition duration-400"
              >
                тонкое
              </button>
              <button
                class="w-[131px] h-[32px] text-[14px] text-[#2C2C2C] font-bold hover:bg-white rounded-[5px] transition duration-400"
              >
                традиционное
              </button>
            </div>
            <div class="w-[265px] m-auto flex justify-between">
              <button
                class="w-[86px] h-[32px] text-[14px] text-[#2C2C2C] font-bold hover:bg-white rounded-[5px] transition duration-400"
                v-for="size in pizza.sizes"
                :key="size"
              >
                {{ size }} см.
              </button>
            </div>
          </div>
          <div class="flex justify-between mt-[17px]">
            <p class="text-[22px] text-[#000000] font-bold">
              от {{ pizza.price }} ₽
            </p>
            <button
              class="w-[132px] h-[40px] flex justify-center items-center border border-[#EB5A1E] rounded-[30px] text-[16px] text-[#EB5A1E] font-bold gap-[7px] hover:bg-[#EB5A1E] hover:text-white transition duration-400"
            >
              <span>+</span>
              <span>Добавить </span>
              <!-- <span>2</span> -->
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
