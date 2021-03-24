<template>
  <div class="bg-gray-900">
    <div class="lg:block hidden">
      <div class="w-full h-screen flex items-center justify-center">
        <div class="lg:w-2/3 w-full h-full bg-gray-800 text-gray-100 flex">
          <div class="mt-14 mx-10 flex flex-col items-center space-y-6">
            <img
              src="~/assets/images/1.jpg"
              class="rounded-xl h-80 w-80 object-cover object-center"
              alt=""
            />

            <h2 class="font-bold text-4xl">$5</h2>
            <p class="text-center text-gray-300">
              Lorem, ipsum dolor sit amet consectetur adipisicing elit. Dolor
              tempore at labore sed molestias soluta asperiores aliquam ipsa
              consequuntur.
            </p>
            <a
              href=""
              class="bg-gray-900 px-10 py-4 rounded-xl text-xl uppercase"
              >Buy Now</a
            >
          </div>

          <div class="mt-14 mx-10 flex flex-col items-center space-y-6">
            <img
              src="~/assets/images/2.jpg"
              class="rounded-xl h-80 w-80 object-cover object-center"
              alt=""
            />

            <h2 class="font-bold text-4xl">$5</h2>
            <p class="text-center text-gray-300">
              Lorem, ipsum dolor sit amet consectetur adipisicing elit. Dolor
              tempore at labore sed molestias soluta asperiores aliquam ipsa
              consequuntur.
            </p>
            <a
              href=""
              class="bg-gray-900 px-10 py-4 rounded-xl text-xl uppercase"
              >Buy Now</a
            >
          </div>

          <div class="mt-14 mx-10 flex flex-col items-center space-y-6">
            <img
              src="~/assets/images/3.jpg"
              class="rounded-xl h-80 w-80 object-cover object-right"
              alt=""
            />

            <h2 class="font-bold text-4xl">$5</h2>
            <p class="text-center text-gray-300">
              Lorem, ipsum dolor sit amet consectetur adipisicing elit. Dolor
              tempore at labore sed molestias soluta asperiores aliquam ipsa
              consequuntur.
            </p>
            <a
              href=""
              class="bg-gray-900 px-10 py-4 rounded-xl text-xl uppercase"
              >Buy Now</a
            >
          </div>
        </div>
      </div>
    </div>

    <div class="lg:hidden block">
      <div class="w-full h-screen flex items-center justify-center">
        <div
          class="lg:w-1/3 w-full h-full bg-gray-800 text-gray-100 lg:invisible visible"
        >
          <swiper class="swiper" ref="mySwiper" :options="swiperOption">
            <swiper-slide>
              <div class="mt-14 mx-10 flex flex-col items-center space-y-6">
                <img
                  src="~/assets/images/1.jpg"
                  class="rounded-xl h-80 w-80 object-cover object-center"
                  alt=""
                />

                <h2 class="font-bold text-4xl">$5</h2>
                <p class="text-center text-gray-300">
                  Lorem, ipsum dolor sit amet consectetur adipisicing elit.
                  Dolor tempore at labore sed molestias soluta asperiores
                  aliquam ipsa consequuntur.
                </p>
                <a
                  href=""
                  class="bg-gray-900 px-10 py-4 rounded-xl text-xl uppercase"
                  >Buy Now</a
                >
              </div>
            </swiper-slide>
            <swiper-slide>
              <div class="mt-14 mx-10 flex flex-col items-center space-y-6">
                <img
                  src="~/assets/images/2.jpg"
                  class="rounded-xl h-80 w-80 object-cover object-center"
                  alt=""
                />

                <h2 class="font-bold text-4xl">$5</h2>
                <p class="text-center text-gray-300">
                  Lorem, ipsum dolor sit amet consectetur adipisicing elit.
                  Dolor tempore at labore sed molestias soluta asperiores
                  aliquam ipsa consequuntur.
                </p>
                <a
                  href=""
                  class="bg-gray-900 px-10 py-4 rounded-xl text-xl uppercase"
                  >Buy Now</a
                >
              </div>
            </swiper-slide>
            <swiper-slide>
              <div class="mt-14 mx-10 flex flex-col items-center space-y-6">
                <img
                  src="~/assets/images/3.jpg"
                  class="rounded-xl h-80 w-80 object-cover object-right"
                  alt=""
                />

                <h2 class="font-bold text-4xl">$5</h2>
                <p class="text-center text-gray-300">
                  Lorem, ipsum dolor sit amet consectetur adipisicing elit.
                  Dolor tempore at labore sed molestias soluta asperiores
                  aliquam ipsa consequuntur.
                </p>
                <a
                  href=""
                  class="bg-gray-900 px-10 py-4 rounded-xl text-xl uppercase"
                  >Buy Now</a
                >
              </div>
            </swiper-slide>
            <div class="swiper-pagination" slot="pagination"></div>
          </swiper>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'carrousel',
  data() {
    return {
      swiperOption: {
        pagination: {
          el: '.swiper-pagination',
        },
        // Some Swiper option/callback...
      },
    }
  },
  computed: {
    swiper() {
      return this.$refs.mySwiper.$swiper
    },
  },
  mounted() {
    this.swiper.slideTo(0, 1000, false)
  },
}
</script>
