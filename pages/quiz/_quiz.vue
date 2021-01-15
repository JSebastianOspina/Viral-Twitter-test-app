<template>
  <div class="flex flex-col w-full intento">
    <div class="flex-auto">
      <div
        class="bg-cover relative w-full h-full flex flex-col justify-center"
        style="background-image: url('/images/pattern.png')"
      >
        <div class="custom-shape-divider-bottom-1610683240">
          <svg
            data-name="Layer 1"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 1200 120"
            preserveAspectRatio="none"
          >
            <path
              d="M985.66,92.83C906.67,72,823.78,31,743.84,14.19c-82.26-17.34-168.06-16.33-250.45.39-57.84,11.73-114,31.07-172,41.86A600.21,600.21,0,0,1,0,27.35V120H1200V95.8C1132.19,118.92,1055.71,111.31,985.66,92.83Z"
              class="shape-fill"
            ></path>
          </svg>
        </div>
        <div class="flex justify-center">
          <img src="/images/logo.png" class="w-40 h-40 ml-2" alt="logo" />
        </div>
        <div>
          <h1
            class="text-5xl text-aguaMarina aguaMarina text-center font-semibold"
          >
            El Bunny
          </h1>
        </div>
      </div>
    </div>
    <div class="flex-auto flex flex-col bg-moradoFondo">
      <p class="text-center font-semibold text-blanco text-3xl">Let's Play!</p>
      <p class="text-center font-semibold text-blanco text-xl">
        Play now and Level up
      </p>
      <div class="flex flex-col justify-end flex-1">
        <a :href="'/quiz/' + $route.params.quiz" 
        class=" py-2 bg-moradoBoton text-center text-blanco text-2xl 
        rounded-2xl mx-6 font-semibold"
        >Play Now</a>
        <a href="/quiz" 
        class="mt-6  mb-12 py-2 text-center text-moradoBoton border border-moradoBoton text-2xl 
        rounded-2xl mx-6 font-semibold"
        >About</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {

  head() {
    return {
      title: this.quiz,
      meta: [
        {
          hid: "description",
          name: "description",
          content: "Receta de " + this.$route.params.quiz,
        },
        {
          hid: "og:description",
          name: "og:description",
          content: "Receta de " + this.$route.params.quiz,
        },
      ],
    };
  },
};
</script>

<style>
.intento{
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
}
.custom-shape-divider-bottom-1610683240 {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  overflow: hidden;
  line-height: 0;
}

.custom-shape-divider-bottom-1610683240 svg {
  position: relative;
  display: block;
  width: calc(100% + 1.3px);
  height: 54px;
}

.custom-shape-divider-bottom-1610683240 .shape-fill {
  fill: #1f1147;
}

/** For tablet devices **/
@media (min-width: 768px) and (max-width: 1023px) {
  .custom-shape-divider-bottom-1610683240 svg {
    width: calc(100% + 1.3px);
    height: 16px;
  }
}
</style>