<template>
  <section class="bg-trading-tools max-w-full sm:mx-4 overflow-hidden mt-[72px]">
    <div class="max-w-screen-xl py-4 px-6 mx-auto">
      <form class="grid md:flex md:flex-row h-screen md:h-auto md:grid-cols-4 gap-8">
        <!-- Letter Head (1st Grid Item) -->
        <div
          class="md:col-span-3 w-full md:w-3/4 h-auto md:h-screen"
          :class="{ 'order-1': $mq === 'sm', 'order-2': $mq === 'md' }"
        >
          <div class="relative z-0 w-full mb-4 group">
            <input
              type="text"
              class="font-patrick-hand block py-2.5 px-0 w-full text-gray-900 bg-transparent border-0 border-b-1 border-gray-100 appearance-none focus:outline-none focus:ring-0 focus:border-primary peer"
              v-model="letterSubject"
              placeholder="A mail from (Date)"
              required
              autofocus
            />
          </div>
          <!-- Letter Body -->
          <div class="h-auto md:h-screen relative">
            <textarea
              type="text"
              class="font-patrick-hand block py-2.5 px-3 w-full text-gray-900 bg-transparent border border-[#0c66ee] rounded-lg focus:outline-none focus:ring-0 focus:border-primary"
              v-model="letterBody"
              placeholder="Dear Future Me,"
              style="resize: none"
              rows="22"
            ></textarea>
          </div>
        </div>

        <!-- Letter Details (2nd Grid Item) -->
        <div class="md:col-span-1 w-full md:w-1/4 text-sm lg:mt-14 sm:mt-2 sm:mb-[56px]">
          <div class="flex flex-col">
            <!-- Time / Periods -->
            <div class="space-x-2 mb-4 flex">
              <button class="time-period-pill selected">3 Months</button>
              <button class="time-period-pill selected">6 Months</button>
              <button class="time-period-pill selected">1 Year</button>
              <button class="time-period-pill">3 Years</button>
              <button class="time-period-pill">5 Years</button>
            </div>

            <!-- Date Picker -->
            <label for="datepicker" class="mb-2 font-bold">Choose a Date:</label>
            <input
              type="date"
              id="datepicker"
              name="datepicker"
              class="p-2 border rounded mb-4 cursor-pointer"
            />

            <!-- Privacy Options -->
            <label class="mb-2 font-bold">Privacy:</label>
            <div class="flex items-center mb-4">
              <input type="radio" name="privacy" value="Private" class="mr-2" />
              <label for="private" class="mr-4">Private</label>
              <input type="radio" name="privacy" value="public" class="mr-2" />
              <label for="public">Public</label>
            </div>

            <!-- Submit Button -->
            <button class="bg-[#0c66ee] text-white py-2 px-4 rounded w-full font-bold">
              Send Letter
            </button>
          </div>
        </div>
      </form>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      letterSubject: "A mail from (Date)",
      letterBody: "Dear future Me,",
      privacy: "private",
    };
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Patrick+Hand&display=swap");

.font-patrick-hand {
  font-family: "Patrick Hand", cursive;
}
</style>
