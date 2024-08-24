<script lang="ts">
  import { onMount } from "svelte";

  let services = [
    {
      name: "Web Development",
      description:
        "We build modern, responsive, and efficient web applications using the latest technologies.",
      imgSrc: "/web-dev.jpg",
    },
    {
      name: "Mobile App Development",
      description:
        "Creating seamless and high-performing mobile applications for Android and iOS platforms.",
      imgSrc: "/mobile-app.jpg",
    },
    {
      name: "Blockchain Solutions",
      description:
        "Innovative blockchain solutions for secure and transparent transactions.",
      imgSrc: "/blockchain-web3.jpg",
    },
    {
      name: "AI and Machine Learning",
      description:
        "Harness the power of AI to drive insights and automation in your business processes.",
      imgSrc: "/ai.png",
    },
    {
      name: "Web Design and Applications Design",
      description:
        "Creativity and innovation in the design of applications which will make your product successful",
      imgSrc: "/web-design.png",
    },
  ];

  let currentIndex = 0;
  let interval: number;

  function nextSlide() {
    currentIndex = (currentIndex + 1) % services.length;
  }

  function prevSlide() {
    currentIndex = (currentIndex - 1 + services.length) % services.length;
  }

  onMount(() => {
    interval = setInterval(nextSlide, 5000);
    return () => clearInterval(interval);
  });
</script>

<div class="carousel text-white">
  <div
    class="carousel-inner"
    style="transform: translateX(-{currentIndex * 100}%)"
  >
    {#each services as service, i}
      <div class="carousel-item">
        <img
          class=" w-full rounded-[12px]"
          src={service.imgSrc}
          alt={service.name}
        />
        <div class="carousel-content">
          <h2 class="text-2xl">{service.name}</h2>
          <p>- {service.description} -</p>
        </div>
      </div>
    {/each}
  </div>
  <button class="carousel-control prev" on:click={prevSlide}>❮</button>
  <button class="carousel-control next" on:click={nextSlide}>❯</button>
</div>

<style>
  .carousel {
    position: relative;
    width: 100%;
    height: 400px;
    overflow: hidden;
  }

  .carousel-inner {
    display: flex;
    transition: transform 0.5s ease;
    height: 100%;
  }

  .carousel-item {
    flex: 0 0 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    padding: 20px;
  }

  .carousel-item img {
    max-width: 100%;
    max-height: 200px;
    object-fit: contain;
    margin-bottom: 20px;
  }

  .carousel-content {
    max-width: 80%;
  }

  .carousel-control {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    background: rgba(0, 0, 0, 0.5);
    color: white;
    border: none;
    padding: 10px 15px;
    cursor: pointer;
    font-size: 18px;
  }

  .prev {
    left: 10px;
  }
  .next {
    right: 10px;
  }
</style>
