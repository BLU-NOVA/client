<div class="relative h-screen w-full bg-deep-space-blue">
  <!-- Background video -->
  <video
    class="absolute opacity-80 top-0 left-0 w-full h-full object-cover"
    autoplay
    muted
    loop
  >
    <source src="/software-bizz-1.mp4" type="video/mp4" />
    Your browser does not support the video tag.
  </video>

  <!-- Overlay to darken the video for better text contrast -->
  <div class="absolute top-0 left-0 w-full h-full bg-black opacity-60"></div>

  <!-- Content on top of the video -->
  <div
    class="relative z-10 flex flex-col items-center justify-center h-full w-full p-6 text-center text-white"
  >
    <h1 class="text-4xl font-bold mb-4 text-electric-blue">About Blu Nova</h1>
    <p class="max-w-lg text-lg mb-6 text-gray-100">
      Blu Nova is a platform that helps you bring your ideas and products to the
      online world. We aim to make digital transformation easy by automating
      repetitive tasks and enabling you to focus on creativity and growth.
    </p>
    <p class="max-w-lg text-lg text-gary-100">
      Our suite of tools and services, from eCommerce to project management, is
      designed to streamline your business processes and enhance your
      productivity.
    </p>
  </div>
</div>

<!-- Additional content section after the video background -->
<div class="py-16 px-6">
  <div class="max-w-4xl mx-auto text-center">
    <h2 class="text-3xl font-bold text-electric-blue mb-4">Our Mission</h2>
    <p class="text-lg text-white mb-6">
      At Blu Nova, our mission is to empower businesses of all sizes to thrive
      in the digital era. We believe in the power of innovation, and we are
      committed to providing tools that simplify your workflow and expand your
      reach.
    </p>

    <!-- Team Section -->
    <h2 class="text-3xl font-bold text-electric-blue mb-8">Meet The Team</h2>
    <div class="flex flex-wrap justify-center gap-8">
      <!-- Team Member 1 -->
      <div class="team-card">
        <div class="card-inner">
          <div class="card-front">
            <img
              src="https://picsum.photos/300/200?random=1"
              alt="Team Member 1"
              class="w-full h-48 object-cover"
            />
            <div class="p-6">
              <h3 class="text-xl font-semibold text-gray-800 mb-2">
                Alice Johnson
              </h3>
              <p class="text-gray-600">Chief Executive Officer</p>
            </div>
          </div>
          <div class="card-back">
            <div class="p-6">
              <h3 class="text-xl font-semibold text-gray-800 mb-2">
                Alice Johnson
              </h3>
              <p class="text-gray-600">Chief Executive Officer</p>
              <p class="mt-4 text-gray-600">
                Alice leads Blu Nova with over 15 years of experience in tech
                innovation, guiding the company to new heights with her vision
                and leadership.
              </p>
            </div>
          </div>
        </div>
      </div>

      <!-- Team Member 2 -->
      <div class="team-card">
        <div class="card-inner">
          <div class="card-front">
            <img
              src="https://picsum.photos/300/200?random=2"
              alt="Team Member 2"
              class="w-full h-48 object-cover"
            />
            <div class="p-6">
              <h3 class="text-xl font-semibold text-gray-800 mb-2">John Doe</h3>
              <p class="text-gray-600">Chief Technology Officer</p>
            </div>
          </div>
          <div class="card-back">
            <div class="p-6">
              <h3 class="text-xl font-semibold text-gray-800 mb-2">John Doe</h3>
              <p class="text-gray-600">Chief Technology Officer</p>
              <p class="mt-4 text-gray-600">
                John oversees all technical aspects of Blu Nova, ensuring our
                platform remains cutting-edge and our customers receive
                top-notch service.
              </p>
            </div>
          </div>
        </div>
      </div>

      <!-- Team Member 3 -->
      <div class="team-card">
        <div class="card-inner">
          <div class="card-front">
            <img
              src="https://picsum.photos/300/200?random=3"
              alt="Team Member 3"
              class="w-full h-48 object-cover"
            />
            <div class="p-6">
              <h3 class="text-xl font-semibold text-gray-800 mb-2">
                Emma Williams
              </h3>
              <p class="text-gray-600">Chief Marketing Officer</p>
            </div>
          </div>
          <div class="card-back">
            <div class="p-6">
              <h3 class="text-xl font-semibold text-gray-800 mb-2">
                Emma Williams
              </h3>
              <p class="text-gray-600">Chief Marketing Officer</p>
              <p class="mt-4 text-gray-600">
                Emma is passionate about connecting people with the right
                solutions, and her marketing strategies have helped Blu Nova
                reach a global audience.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<style>
  .team-card {
    perspective: 1000px;
    width: 100%;
    max-width: 300px;
    height: 400px;
  }

  .card-inner {
    position: relative;
    width: 100%;
    height: 100%;
    text-align: center;
    transition: transform 0.6s;
    transform-style: preserve-3d;
  }

  .team-card:hover .card-inner {
    transform: rotateY(180deg);
  }

  .card-front,
  .card-back {
    position: absolute;
    width: 100%;
    height: 100%;
    backface-visibility: hidden;
    background-color: #f3f4f6;
    border-radius: 0.5rem;
    overflow: hidden;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  }

  .card-back {
    transform: rotateY(180deg);
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 1rem;
  }
</style>
