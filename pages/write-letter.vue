<template>
  <section class="bg-trading-tools max-w-full sm:mx-4 overflow-hidden">
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
              class="font-patrick-hand block py-2.5 px-3 w-full text-gray-900 bg-transparent border-1 border-[#0c66ee] rounded-lg focus:outline-none focus:ring-0 focus:border-primary"
              v-model="letterBody"
              placeholder="Dear Future Me,"
              style="resize: none"
              rows="22"
            ></textarea>
          </div>
        </div>

        <!-- Letter Details (2nd Grid Item) -->
        <div class="md:col-span-1 w-full md:w-1/4 text-sm mt-14">
          <p>Delivery Date</p>
          <div>6 months</div>
          <div>6 months</div>
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
