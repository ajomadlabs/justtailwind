<template>
  <div>
    <!-- MAIN SECTION -->
    <center>
      <div
        style="max-width: 1180px"
      >
        <!-- CARD SECTION -->
        <div
          class="mt-20 lg:flex lg:flex-wrap lg:items-start"
        >
          <!-- CONTENT SECTION -->
          <div
            v-for="(card, i) in cards"
            :key="i"
            class="bg-gray-800 px-4 py-6 cursor-pointer rounded-lg xs:w-10/12 md:w-4/12 lg:w-3/12"
            :class="i == 0 ? 'ml-0' : 'ml-2'"
          >
            <!-- IMAGE SECTION -->
            <div
              class="bg-yellow-300 cursor-pointer w-full h-36 py-18 rounded-lg"
              @click="$router.push('/design/' + card.number)"
            >
              <h3
                class="leading-normal tracking-normal antialiased text-just-tailwind-black font-bold text-22"
              >
                Design #{{ card.number}}
              </h3>
            </div>
            <!-- END -->

            <!-- CARD INFO -->
            <div
              class="mt-2"
            >
              <p
                class="leading-normal tracking-normal antialiased text-20 text-left text-gray-300 font-medium"
              >
                {{ card.desc }}
              </p>
              <p
                class="leading-normal tracking-normal antialiased text-12 text-left text-gray-300 font-medium"
              >
                Designer: {{ card.designer }}
              </p>
            </div>

          </div>
          <!-- END -->
        </div>
        <!-- END -->

      </div>
    </center>
    <!-- END -->
  </div>
</template>

<script>
export default {
  head () {
    return {
      bodyAttrs: {
        class: ["bg-gray-900"]
      }
    }
  },
  data () {
    return {
      cards: [
        {
          number: '01',
          desc: "Threapy Profile",
          designer: "Ben George"
        }
      ]
    }
  }
}
</script>
