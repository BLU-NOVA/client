<script>
  // Add any necessary imports here

  // You may want to make these dynamic if the data might change
  const communityLinks = [
    { text: "Tutorials", href: "#" },
    { text: "Documentation", href: "#" },
    { text: "Forum", href: "#" },
  ];

  const openSourceLinks = [
    { text: "Download", href: "#" },
    { text: "Github", href: "#" },
    { text: "Runbot", href: "#" },
    { text: "Translations", href: "#" },
  ];

  const servicesLinks = [
    { text: "Blu Nova Hosting", href: "#" },
    { text: "Support", href: "#" },
    { text: "Upgrade", href: "#" },
    { text: "Custom Developments", href: "#" },
    { text: "Education", href: "#" },
    { text: "Find an Accountant", href: "#" },
    { text: "Find a Partner", href: "#" },
    { text: "Become a Partner", href: "#" },
  ];

  const aboutUsLinks = [
    { text: "Our company", href: "#" },
    { text: "Brand Assets", href: "#" },
    { text: "Contact us", href: "#" },
    { text: "Jobs", href: "#" },
    { text: "Events", href: "#" },
    { text: "Podcast", href: "#" },
    { text: "Blog", href: "#" },
    { text: "Customers", href: "#" },
    { text: "Legal • Privacy", href: "#" },
    { text: "Security", href: "#" },
  ];

  const socialLinks = [
    { icon: "facebook-f", href: "#" },
    { icon: "twitter", href: "#" },
    { icon: "linkedin-in", href: "#" },
    { icon: "github", href: "#" },
    { icon: "instagram", href: "#" },
    { icon: "tiktok", href: "#" },
    { icon: "phone", href: "#" },
  ];
</script>

<footer class="bg-deep-space-blue text-gray-400 py-10 px-5 font-sans">
  <div class="max-w-screen-lg mx-auto flex flex-wrap">
    <div class="mb-8">
      <img src="/blu-bgless.png" alt="Blu Nova" class="max-w-[100px] mb-5" />
    </div>

    <div class="flex flex-wrap justify-between w-full">
      <div class="flex-1 min-w-[200px] mb-8 pr-5">
        <h3 class="text-white text-xl mb-4">Community</h3>
        <ul>
          {#each communityLinks as link}
            <li class="mb-2">
              <a href={link.href} class="text-gray-400 hover:text-white"
                >{link.text}</a
              >
            </li>
          {/each}
        </ul>

        <h3 class="text-white text-xl mt-6 mb-4">Open Source</h3>
        <ul>
          {#each openSourceLinks as link}
            <li class="mb-2">
              <a href={link.href} class="text-gray-400 hover:text-white"
                >{link.text}</a
              >
            </li>
          {/each}
        </ul>
      </div>

      <div class="flex-1 min-w-[200px] mb-8 pr-5">
        <h3 class="text-white text-xl mb-4">Services</h3>
        <ul>
          {#each servicesLinks as link}
            <li class="mb-2">
              <a href={link.href} class="text-gray-400 hover:text-white"
                >{link.text}</a
              >
            </li>
          {/each}
        </ul>
      </div>

      <div class="flex-1 min-w-[200px] mb-8">
        <h3 class="text-white text-xl mb-4">About us</h3>
        <ul>
          {#each aboutUsLinks as link}
            <li class="mb-2">
              <a href={link.href} class="text-gray-400 hover:text-white"
                >{link.text}</a
              >
            </li>
          {/each}
        </ul>
      </div>

      <div class="flex-1 min-w-[200px] mb-8">
        <div class="mb-5">
          <span class="inline-block mr-2 text-xl">🇺🇸</span> English ▼
        </div>

        <p class="mb-4">
          Blu Nova is a platform designed to help individuals and businesses
          bring their ideas and products to market online. It streamlines and
          automates repetitive office tasks, freeing you from mundane work and
          allowing you to focus on what truly matters—growing and innovating.
        </p>

        <p class="mb-4">
          Blu Nova's unique value proposition is to be at the same time very
          easy to use and fully integrated.
        </p>

        <div class="flex space-x-3 mt-5">
          {#each socialLinks as link}
            <a
              href={link.href}
              class="w-8 h-8 bg-gray-400 rounded-full flex items-center justify-center text-white"
            >
              <i class={`fab fa-${link.icon}`}></i>
            </a>
          {/each}
        </div>
      </div>
    </div>
  </div>

  <div class="text-center mt-10 pt-5 border-t border-gray-600">
    <p>Website made by Blu Nova</p>
  </div>
</footer>
