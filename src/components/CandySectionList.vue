<script>
import CandySectionItem from './checkout/CandySectionItem.vue'
  export default {
    props: {
      candy: {
        type: Array,
        required: true
      }
    },
    components: {
      CandySectionItem
    },
    data() {
      return {
        checkoutPrice: 0,
        checkoutItems: [],
      }
    },
    methods: {
      addToCart(price) {
        // add the selected items to the cart
        // const item = this.candy.find(sweet => sweet.id === this.sweet.id)
        console.log(price)
        this.checkoutItems.push(price)
      }
    },
  }
</script>
<template>
  <section class="bg-white dark:bg-gray-900">
    <div class="container px-6 py-8 mx-auto">
      <div class="lg:flex lg:-mx-2">
        <div class="space-y-3 lg:w-1/5 lg:px-2 lg:space-y-4">
          <a
            href="#"
            class="block font-medium text-gray-500 dark:text-gray-300 hover:underline"
            >Candy Bars</a
          >
          <a
            href="#"
            class="block font-medium text-gray-500 dark:text-gray-300 hover:underline"
            >Candy Canes</a
          >
          <a
            href="#"
            class="block font-medium text-blue-600 dark:text-blue-500 hover:underline"
            >Bite Size</a
          >
          <a
            href="#"
            class="block font-medium text-gray-500 dark:text-gray-300 hover:underline"
            >Bon Bons</a
          >
          <a
            href="#"
            class="block font-medium text-gray-500 dark:text-gray-300 hover:underline"
            >Chocolate</a
          >
        </div>

        <div class="mt-6 lg:mt-0 lg:px-2 lg:w-4/5">
          <div
            class="flex items-center justify-between text-sm tracking-widest uppercase"
          >
            <p class="text-gray-500 dark:text-gray-300">6 Items</p>
            <div class="flex items-center">
              <p class="text-gray-500 dark:text-gray-300">Sort</p>
              <select
                class="font-medium text-gray-700 bg-transparent dark:text-gray-500 focus:outline-none"
              >
                <option value="#">Recommended</option>
                <option value="#">Size</option>
                <option value="#">Price</option>
              </select>
            </div>
          </div>
          <!-- List starts here..... -->
          <div
            class="grid grid-cols-1 gap-8 mt-8 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4"
          >
            <CandySectionItem v-for="(item, index) in candy" :sweet="item" :key="index" @addToCart="addToCart" />
 
            <div
              class="flex flex-col items-center justify-center w-full max-w-lg mx-auto"
            >
              <img
                class="object-cover w-full rounded-md h-72 xl:h-80"
                src="https://images.unsplash.com/photo-1565004602745-718e1b0d44f8?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8NDJ8fHN3ZWV0fGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60"
                alt="IcePan"
              />
              <h4 class="mt-2 text-lg font-medium text-gray-700 dark:text-gray-200">
                IceCream Pancakes
              </h4>
              <p class="text-blue-500">$16.55</p>

              <button
                class="flex items-center justify-center w-full px-2 py-2 mt-4 font-medium tracking-wide text-white capitalize transition-colors duration-200 transform bg-gray-800 rounded-md hover:bg-gray-700 focus:outline-none focus:bg-gray-700"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="w-5 h-5 mx-1"
                  viewBox="0 0 20 20"
                  fill="currentColor"
                >
                  <path
                    d="M3 1a1 1 0 000 2h1.22l.305 1.222a.997.997 0 00.01.042l1.358 5.43-.893.892C3.74 11.846 4.632 14 6.414 14H15a1 1 0 000-2H6.414l1-1H14a1 1 0 00.894-.553l3-6A1 1 0 0017 3H6.28l-.31-1.243A1 1 0 005 1H3zM16 16.5a1.5 1.5 0 11-3 0 1.5 1.5 0 013 0zM6.5 18a1.5 1.5 0 100-3 1.5 1.5 0 000 3z"
                  />
                </svg>
                <span class="mx-1">Add to cart</span>
              </button>
            </div>

            <div
              class="flex flex-col items-center justify-center w-full max-w-lg mx-auto"
            >
              <img
                class="object-cover w-full rounded-md h-72 xl:h-80"
                src="https://images.unsplash.com/photo-1567327613485-fbc7bf196198?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8NTF8fHN3ZWV0fGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60"
                alt="Blueberry"
              />
              <h4 class="mt-2 text-lg font-medium text-gray-700 dark:text-gray-200">
                Blueberry Cake
              </h4>
              <p class="text-blue-500">$12.55</p>

              <button
                class="flex items-center justify-center w-full px-2 py-2 mt-4 font-medium tracking-wide text-white capitalize transition-colors duration-200 transform bg-gray-800 rounded-md hover:bg-gray-700 focus:outline-none focus:bg-gray-700"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="w-5 h-5 mx-1"
                  viewBox="0 0 20 20"
                  fill="currentColor"
                >
                  <path
                    d="M3 1a1 1 0 000 2h1.22l.305 1.222a.997.997 0 00.01.042l1.358 5.43-.893.892C3.74 11.846 4.632 14 6.414 14H15a1 1 0 000-2H6.414l1-1H14a1 1 0 00.894-.553l3-6A1 1 0 0017 3H6.28l-.31-1.243A1 1 0 005 1H3zM16 16.5a1.5 1.5 0 11-3 0 1.5 1.5 0 013 0zM6.5 18a1.5 1.5 0 100-3 1.5 1.5 0 000 3z"
                  />
                </svg>
                <span class="mx-1">Add to cart</span>
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
