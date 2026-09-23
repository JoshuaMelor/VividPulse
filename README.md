<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="VividPulse Creative — Scroll-stopping design and social media strategy that scales." />
  <title>VividPulse Creative — Design & Social Growth</title>

  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>

  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            ink: "#09090b",
            panel: "#111116",
            violet: "#8B5CF6",
            cyan: "#22D3EE",
          },
          fontFamily: {
            sans: ["Inter", "ui-sans-serif", "system-ui", "sans-serif"],
          },
          boxShadow: {
            glow: "0 0 40px rgba(139,92,246,.25)",
            cyanGlow: "0 0 40px rgba(34,211,238,.2)",
          },
        },
      },
    };
  </script>

  <style>
    html {
      scroll-behavior: smooth;
    }

    body {
      background: #09090b;
      color: #f4f4f5;
    }

    .gradient-text {
      background: linear-gradient(90deg, #fff, #a78bfa, #67e8f9);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }

    .grid-bg {
      background-image:
        linear-gradient(rgba(255,255,255,.035) 1px, transparent 1px),
        linear-gradient(90deg, rgba(255,255,255,.035) 1px, transparent 1px);
      background-size: 42px 42px;
    }

    .noise {
      background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 180 180' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.9' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='.035'/%3E%3C/svg%3E");
    }

    .service-card,
    .portfolio-card {
      transition: transform .35s ease, border-color .35s ease, box-shadow .35s ease;
    }

    .service-card:hover,
    .portfolio-card:hover {
      transform: translateY(-8px);
      border-color: rgba(139, 92, 246, .6);
      box-shadow: 0 20px 60px rgba(139, 92, 246, .12);
    }

    .portfolio-card img {
      transition: transform .6s ease;
    }

    .portfolio-card:hover img {
      transform: scale(1.06);
    }

    .orb {
      animation: float 7s ease-in-out infinite;
    }

    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-20px); }
    }

    .reveal {
      opacity: 0;
      transform: translateY(24px);
      transition: opacity .7s ease, transform .7s ease;
    }

    .reveal.visible {
      opacity: 1;
      transform: translateY(0);
    }
  </style>
</head>

<body class="font-sans antialiased overflow-x-hidden">

  <!-- ================= HEADER ================= -->
  <header class="fixed top-0 left-0 right-0 z-50 border-b border-white/5 bg-black/70 backdrop-blur-xl">
    <nav class="max-w-7xl mx-auto px-6 lg:px-8 h-20 flex items-center justify-between">
      <a href="#" class="text-xl font-black tracking-tight">
        Vivid<span class="text-violet">Pulse</span>
      </a>

      <!-- Desktop navigation -->
      <div class="hidden md:flex items-center gap-8 text-sm text-zinc-400">
        <a href="#services" class="hover:text-white transition">Services</a>
        <a href="#work" class="hover:text-white transition">Work</a>
        <a href="#results" class="hover:text-white transition">Results</a>
        <a href="#contact" class="hover:text-white transition">Contact</a>
      </div>

      <a href="#contact"
         class="hidden md:inline-flex rounded-full bg-white px-5 py-2.5 text-sm font-bold text-black hover:bg-cyan-300 transition">
        Book a Free Audit
      </a>

      <!-- Mobile menu button -->
      <button id="menuBtn"
              aria-label="Open navigation"
              aria-expanded="false"
              class="md:hidden text-zinc-300">
        <svg class="w-7 h-7" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.8"
                d="M4 6h16M4 12h16M4 18h16"/>
        </svg>
      </button>
    </nav>

    <!-- Mobile navigation -->
    <div id="mobileMenu" class="hidden md:hidden border-t border-white/5 bg-black/95">
      <div class="px-6 py-6 flex flex-col gap-5 text-zinc-300">
        <a href="#services" class="mobile-link">Services</a>
        <a href="#work" class="mobile-link">Work</a>
        <a href="#results" class="mobile-link">Results</a>
        <a href="#contact" class="mobile-link">Contact</a>
        <a href="#contact" class="rounded-full bg-violet-500 px-5 py-3 text-center font-bold text-white">
          Book a Free Audit
        </a>
      </div>
    </div>
  </header>


  <main>

    <!-- ================= HERO ================= -->
    <section class="relative min-h-screen flex items-center overflow-hidden grid-bg">
      <div class="absolute inset-0 noise pointer-events-none"></div>

      <!-- Decorative glows -->
      <div class="orb absolute -top-32 -right-32 w-96 h-96 rounded-full bg-violet-600/20 blur-[100px]"></div>
      <div class="orb absolute bottom-0 -left-32 w-96 h-96 rounded-full bg-cyan-400/10 blur-[100px]"
           style="animation-delay: -3s"></div>

      <div class="relative max-w-7xl mx-auto px-6 lg:px-8 pt-32 pb-20">
        <div class="max-w-5xl reveal">

          <div class="inline-flex items-center gap-2 rounded-full border border-white/10 bg-white/5 px-4 py-2 text-xs uppercase tracking-[.2em] text-zinc-400 mb-8">
            <span class="w-2 h-2 rounded-full bg-cyan-400 shadow-[0_0_12px_#22d3ee]"></span>
            Creative growth partner
          </div>

          <h1 class="text-5xl sm:text-6xl lg:text-8xl font-black tracking-[-.055em] leading-[.95]">
            Scroll-stopping design.
            <span class="gradient-text">Strategy that scales.</span>
          </h1>

          <p class="mt-8 max-w-2xl text-lg md:text-xl leading-relaxed text-zinc-400">
            We build distinctive visual identities and social media systems
            that help ambitious brands get noticed, remembered, and chosen.
          </p>

          <div class="mt-10 flex flex-col sm:flex-row gap-4">
            <a href="#contact"
               class="group inline-flex items-center justify-center gap-3 rounded-full bg-violet-500 px-7 py-4 font-bold text-white shadow-glow hover:bg-violet-400 transition">
              Book a Free Audit
              <span class="group-hover:translate-x-1 transition">→</span>
            </a>

            <a href="#work"
               class="inline-flex items-center justify-center rounded-full border border-white/10 bg-white/5 px-7 py-4 font-semibold text-zinc-200 hover:bg-white/10 transition">
              Explore Our Work
            </a>
          </div>
        </div>

        <!-- Hero stats -->
        <div class="mt-20 grid grid-cols-2 md:grid-cols-4 gap-6 border-t border-white/10 pt-8 reveal">
          <div>
            <p class="text-3xl font-black">2M+</p>
            <p class="text-sm text-zinc-500 mt-1">Organic views</p>
          </div>
          <div>
            <p class="text-3xl font-black">80+</p>
            <p class="text-sm text-zinc-500 mt-1">Brands elevated</p>
          </div>
          <div>
            <p class="text-3xl font-black">4.8×</p>
            <p class="text-sm text-zinc-500 mt-1">Average engagement lift</p>
          </div>
          <div>
            <p class="text-3xl font-black">24/7</p>
            <p class="text-sm text-zinc-500 mt-1">Creative momentum</p>
          </div>
        </div>
      </div>
    </section>


    <!-- ================= SERVICES ================= -->
    <section id="services" class="py-28 lg:py-36 bg-[#0d0d11]">
      <div class="max-w-7xl mx-auto px-6 lg:px-8">

        <div class="max-w-2xl reveal">
          <p class="text-sm font-bold uppercase tracking-[.25em] text-cyan-400">
            What we do
          </p>
          <h2 class="mt-4 text-4xl md:text-6xl font-black tracking-tight">
            Creative that moves <span class="text-zinc-500">business.</span>
          </h2>
          <p class="mt-6 text-zinc-400 text-lg">
            From the first visual impression to the daily content engine,
            we turn your brand into something people want to follow.
          </p>
        </div>

        <div class="grid md:grid-cols-2 gap-6 mt-16">

          <!-- Graphic Design -->
          <article class="service-card group relative overflow-hidden rounded-3xl border border-white/10 bg-[#111116] p-8 md:p-10 reveal">
            <div class="absolute -right-20 -top-20 w-64 h-64 rounded-full bg-violet-500/10 blur-3xl"></div>

            <div class="relative">
              <div class="w-14 h-14 rounded-2xl bg-violet-500/10 border border-violet-400/20 flex items-center justify-center text-violet-400">
                <svg class="w-7 h-7" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-width="1.5" d="M4 4h16v16H4zM8 8h8M8 12h5M8 16h8"/>
                </svg>
              </div>

              <p class="mt-10 text-sm uppercase tracking-[.2em] text-violet-400 font-bold">
                01 / Visual Identity
              </p>

              <h3 class="mt-3 text-3xl md:text-4xl font-black">
                Graphic Design
              </h3>

              <p class="mt-5 text-zinc-400 leading-relaxed">
                Build a visual identity your audience recognizes instantly —
                from brand systems and packaging to social graphics and campaigns.
              </p>

              <ul class="mt-8 space-y-3 text-sm text-zinc-300">
                <li>✦ Brand identity & visual systems</li>
                <li>✦ Custom social media graphics</li>
                <li>✦ Packaging & marketing assets</li>
                <li>✦ Campaign concepts & art direction</li>
              </ul>

              <a href="#contact" class="inline-flex mt-10 text-sm font-bold text-white group-hover:text-cyan-300 transition">
                Build your visual edge →
              </a>
            </div>
          </article>

          <!-- Social Media -->
          <article class="service-card group relative overflow-hidden rounded-3xl border border-white/10 bg-[#111116] p-8 md:p-10 reveal">
            <div class="absolute -right-20 -top-20 w-64 h-64 rounded-full bg-cyan-400/10 blur-3xl"></div>

            <div class="relative">
              <div class="w-14 h-14 rounded-2xl bg-cyan-400/10 border border-cyan-300/20 flex items-center justify-center text-cyan-300">
                <svg class="w-7 h-7" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-width="1.5" d="M7 8h10M7 12h6M5 19l-1 2 4-1h10a3 3 0 003-3V7a3 3 0 00-3-3H6a3 3 0 00-3 3v9a3 3 0 003 3h1"/>
                </svg>
              </div>

              <p class="mt-10 text-sm uppercase tracking-[.2em] text-cyan-300 font-bold">
                02 / Social Growth
              </p>

              <h3 class="mt-3 text-3xl md:text-4xl font-black">
                Social Media Management
              </h3>

              <p class="mt-5 text-zinc-400 leading-relaxed">
                Turn your social channels into a consistent growth engine with
                strategic content, community engagement, and performance-led iteration.
              </p>

              <ul class="mt-8 space-y-3 text-sm text-zinc-300">
                <li>✦ Strategy & monthly content planning</li>
                <li>✦ Content creation & publishing</li>
                <li>✦ Community management</li>
                <li>✦ Analytics & growth optimization</li>
              </ul>

              <a href="#contact" class="inline-flex mt-10 text-sm font-bold text-white group-hover:text-cyan-300 transition">
                Grow your social presence →
              </a>
            </div>
          </article>

        </div>
      </div>
    </section>


    <!-- ================= PORTFOLIO ================= -->
    <section id="work" class="py-28 lg:py-36">
      <div class="max-w-7xl mx-auto px-6 lg:px-8">

        <div class="flex flex-col md:flex-row md:items-end justify-between gap-6 reveal">
          <div>
            <p class="text-sm font-bold uppercase tracking-[.25em] text-violet-400">
              Selected work
            </p>
            <h2 class="mt-4 text-4xl md:text-6xl font-black tracking-tight">
              Made to be <span class="gradient-text">seen.</span>
            </h2>
          </div>

          <p class="max-w-md text-zinc-500">
            A snapshot of the visual worlds we've created for brands ready
            to stand apart.
          </p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-5 mt-16">

          <article class="portfolio-card group relative overflow-hidden rounded-3xl border border-white/10 bg-panel md:col-span-2 reveal">
            <img
              src="https://images.unsplash.com/photo-1558655146-d09347e92766?auto=format&fit=crop&w=1400&q=85"
              alt="Creative branding project"
              class="w-full h-[420px] object-cover"
              loading="lazy"
            />
            <div class="absolute inset-0 bg-gradient-to-t from-black via-black/20 to-transparent"></div>
            <div class="absolute bottom-0 left-0 p-7">
              <p class="text-xs uppercase tracking-[.2em] text-cyan-300">Brand Identity</p>
              <h3 class="mt-2 text-2xl font-black">Future / Form</h3>
            </div>
          </article>

          <article class="portfolio-card group relative overflow-hidden rounded-3xl border border-white/10 bg-panel reveal">
            <img
              src="https://images.unsplash.com/photo-1618005198919-d3d4b5a92ead?auto=format&fit=crop&w=900&q=85"
              alt="Abstract social media campaign"
              class="w-full h-[420px] object-cover"
              loading="lazy"
            />
            <div class="absolute inset-0 bg-gradient-to-t from-black via-transparent to-transparent"></div>
            <div class="absolute bottom-0 left-0 p-7">
              <p class="text-xs uppercase tracking-[.2em] text-violet-300">Campaign</p>
              <h3 class="mt-2 text-2xl font-black">Neon Culture</h3>
            </div>
          </article>

          <article class="portfolio-card group relative overflow-hidden rounded-3xl border border-white/10 bg-panel reveal">
            <img
              src="https://images.unsplash.com/photo-1561070791-2526d30994b5?auto=format&fit=crop&w=900&q=85"
              alt="Brand design workspace"
              class="w-full h-[420px] object-cover"
              loading="lazy"
            />
            <div class="absolute inset-0 bg-gradient-to-t from-black via-transparent to-transparent"></div>
            <div class="absolute bottom-0 left-0 p-7">
              <p class="text-xs uppercase tracking-[.2em] text-cyan-300">Visual System</p>
              <h3 class="mt-2 text-2xl font-black">Mono Haus</h3>
            </div>
          </article>

          <article class="portfolio-card group relative overflow-hidden rounded-3xl border border-white/10 bg-panel md:col-span-2 reveal">
            <img
              src="https://images.unsplash.com/photo-1634942537034-2531766767d1?auto=format&fit=crop&w=1400&q=85"
              alt="Colorful creative campaign"
              class="w-full h-[420px] object-cover"
              loading="lazy"
            />
            <div class="absolute inset-0 bg-gradient-to-t from-black via-black/10 to-transparent"></div>
            <div class="absolute bottom-0 left-0 p-7">
              <p class="text-xs uppercase tracking-[.2em] text-violet-300">Social Campaign</p>
              <h3 class="mt-2 text-2xl font-black">Electric Everyday</h3>
            </div>
          </article>

        </div>
      </div>
    </section>


    <!-- ================= RESULTS ================= -->
    <section id="results" class="py-28 bg-[#0d0d11] border-y border-white/5">
      <div class="max-w-7xl mx-auto px-6 lg:px-8">

        <div class="grid lg:grid-cols-2 gap-16 items-start">

          <div class="reveal">
            <p class="text-sm font-bold uppercase tracking-[.25em] text-cyan-400">
              The impact
            </p>

            <h2 class="mt-4 text-4xl md:text-6xl font-black tracking-tight">
              Pretty is good.
              <span class="text-zinc-500">Performance is better.</span>
            </h2>

            <p class="mt-6 text-zinc-400 text-lg leading-relaxed">
              We connect creative decisions to measurable business outcomes,
              so your content doesn't just look good — it has a job to do.
            </p>

            <div class="grid grid-cols-2 gap-8 mt-12">
              <div>
                <p class="text-4xl font-black gradient-text">2M+</p>
                <p class="mt-2 text-sm text-zinc-500">Organic views generated</p>
              </div>

              <div>
                <p class="text-4xl font-black gradient-text">310%</p>
                <p class="mt-2 text-sm text-zinc-500">Highest engagement growth</p>
              </div>

              <div>
                <p class="text-4xl font-black gradient-text">80+</p>
                <p class="mt-2 text-sm text-zinc-500">Brands supported</p>
              </div>

              <div>
                <p class="text-4xl font-black gradient-text">4.8/5</p>
                <p class="mt-2 text-sm text-zinc-500">Average client rating</p>
              </div>
            </div>
          </div>

          <!-- Testimonials -->
          <div class="space-y-5 reveal">

            <blockquote class="rounded-3xl border border-white/10 bg-black/30 p-8">
              <div class="text-cyan-300 text-xl">★★★★★</div>
              <p class="mt-5 text-lg leading-relaxed text-zinc-200">
                “VividPulse completely changed how our brand shows up online.
                Our content finally feels cohesive, premium, and unmistakably us.”
              </p>
              <footer class="mt-7">
                <p class="font-bold">Maya Rodriguez</p>
                <p class="text-sm text-zinc-500">Founder, Forma Studio</p>
              </footer>
            </blockquote>

            <blockquote class="rounded-3xl border border-white/10 bg-black/30 p-8">
              <div class="text-violet-300 text-xl">★★★★★</div>
              <p class="mt-5 text-lg leading-relaxed text-zinc-200">
                “They didn't just make us better looking. They gave us a
                repeatable content system that our team can actually scale.”
              </p>
              <footer class="mt-7">
                <p class="font-bold">Jordan Lee</p>
                <p class="text-sm text-zinc-500">Co-founder, Northstar Goods</p>
              </footer>
            </blockquote>

          </div>
        </div>
      </div>
    </section>


    <!-- ================= CONTACT ================= -->
    <section id="contact" class="relative py-28 lg:py-36 overflow-hidden">
      <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[500px] h-[500px] bg-violet-600/10 blur-[130px] rounded-full"></div>

      <div class="relative max-w-7xl mx-auto px-6 lg:px-8">
        <div class="grid lg:grid-cols-2 gap-16">

          <div class="reveal">
            <p class="text-sm font-bold uppercase tracking-[.25em] text-violet-400">
              Start a conversation
            </p>

            <h2 class="mt-4 text-5xl md:text-7xl font-black tracking-[-.04em] leading-none">
              Ready to make
              <span class="gradient-text">some noise?</span>
            </h2>

            <p class="mt-7 max-w-lg text-lg text-zinc-400 leading-relaxed">
              Tell us where your brand is today and where you want it to go.
              We'll come prepared with ideas.
            </p>

            <div class="mt-10 space-y-5 text-sm text-zinc-400">
              <div class="flex gap-4">
                <span class="text-cyan-300">01</span>
                <span>Complete the quick discovery form.</span>
              </div>
              <div class="flex gap-4">
                <span class="text-cyan-300">02</span>
                <span>We'll review your brand and goals.</span>
              </div>
              <div class="flex gap-4">
                <span class="text-cyan-300">03</span>
                <span>We'll jump on a no-pressure strategy call.</span>
              </div>
            </div>
          </div>

          <!-- Inquiry form -->
          <form id="inquiryForm"
                class="rounded-3xl border border-white/10 bg-white/[.03] p-7 md:p-9 backdrop-blur reveal">

            <div class="grid sm:grid-cols-2 gap-5">

              <div class="sm:col-span-2">
                <label for="name" class="block text-sm font-medium text-zinc-300 mb-2">
                  Name
                </label>
                <input
                  id="name"
                  name="name"
                  type="text"
                  required
                  placeholder="Your name"
                  class="w-full rounded-xl border border-white/10 bg-black/40 px-4 py-3.5 text-white placeholder-zinc-600 outline-none focus:border-violet-400 transition"
                />
              </div>

              <div class="sm:col-span-2">
                <label for="email" class="block text-sm font-medium text-zinc-300 mb-2">
                  Email
                </label>
                <input
                  id="email"
                  name="email"
                  type="email"
                  required
                  placeholder="you@company.com"
                  class="w-full rounded-xl border border-white/10 bg-black/40 px-4 py-3.5 text-white placeholder-zinc-600 outline-none focus:border-violet-400 transition"
                />
              </div>

              <div>
                <label for="need" class="block text-sm font-medium text-zinc-300 mb-2">
                  Primary Need
                </label>
                <select
                  id="need"
                  name="need"
                  required
                  class="w-full rounded-xl border border-white/10 bg-black/40 px-4 py-3.5 text-white outline-none focus:border-violet-400 transition"
                >
                  <option value="" disabled selected>Select one</option>
                  <option>Graphic Design</option>
                  <option>Social Media</option>
                  <option>Both</option>
                </select>
              </div>

              <div>
                <label for="budget" class="block text-sm font-medium text-zinc-300 mb-2">
                  Project Budget
                </label>
                <select
                  id="budget"
                  name="budget"
                  required
                  class="w-full rounded-xl border border-white/10 bg-black/40 px-4 py-3.5 text-white outline-none focus:border-violet-400 transition"
                >
                  <option value="" disabled selected>Select range</option>
                  <option>Under $1,000</option>
                  <option>$1,000 – $2,500</option>
                  <option>$2,500 – $5,000</option>
                  <option>$5,000 – $10,000</option>
                  <option>$10,000+</option>
                </select>
              </div>

              <div class="sm:col-span-2">
                <label for="message" class="block text-sm font-medium text-zinc-300 mb-2">
                  Tell us about the project
                </label>
                <textarea
                  id="message"
                  name="message"
                  rows="5"
                  placeholder="What are you trying to achieve?"
                  class="w-full rounded-xl border border-white/10 bg-black/40 px-4 py-3.5 text-white placeholder-zinc-600 outline-none focus:border-violet-400 transition resize-none"
                ></textarea>
              </div>

            </div>

            <button
              type="submit"
              class="mt-6 w-full rounded-xl bg-violet-500 py-4 font-bold text-white shadow-glow hover:bg-violet-400 transition"
            >
              Request My Free Audit →
            </button>

            <p id="formMessage" class="hidden mt-4 text-center text-sm text-cyan-300"></p>

            <p class="mt-5 text-center text-xs text-zinc-600">
              No spam. No hard sell. Just useful ideas for your brand.
            </p>
          </form>

        </div>
      </div>
    </section>

  </main>


  <!-- ================= FOOTER ================= -->
  <footer class="border-t border-white/5 bg-black">
    <div class="max-w-7xl mx-auto px-6 lg:px-8 py-10">
      <div class="flex flex-col md:flex-row items-center justify-between gap-5">

        <div>
          <p class="text-lg font-black">
            Vivid<span class="text-violet-400">Pulse</span>
          </p>
          <p class="mt-1 text-sm text-zinc-600">
            Creative strategy for brands with ambition.
          </p>
        </div>

        <div class="flex gap-6 text-sm text-zinc-500">
          <a href="#" class="hover:text-white transition">Instagram</a>
          <a href="#" class="hover:text-white transition">LinkedIn</a>
          <a href="#" class="hover:text-white transition">Behance</a>
        </div>

        <p class="text-xs text-zinc-700">
          © 2026 VividPulse Creative
        </p>
      </div>
    </div>
  </footer>


  <!-- ================= JAVASCRIPT ================= -->
  <script>
    // Mobile navigation toggle
    const menuBtn = document.getElementById("menuBtn");
    const mobileMenu = document.getElementById("mobileMenu");

    menuBtn.addEventListener("click", () => {
      const isOpen = !mobileMenu.classList.contains("hidden");

      mobileMenu.classList.toggle("hidden");
      menuBtn.setAttribute("aria-expanded", String(!isOpen));
    });

    // Close mobile menu after navigation
    document.querySelectorAll(".mobile-link").forEach(link => {
      link.addEventListener("click", () => {
        mobileMenu.classList.add("hidden");
        menuBtn.setAttribute("aria-expanded", "false");
      });
    });

    // Scroll reveal animation
    const revealElements = document.querySelectorAll(".reveal");

    const observer = new IntersectionObserver(
      entries => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            entry.target.classList.add("visible");
            observer.unobserve(entry.target);
          }
        });
      },
      {
        threshold: 0.12
      }
    );

    revealElements.forEach(element => observer.observe(element));

    // Demo form handling
    const form = document.getElementById("inquiryForm");
    const formMessage = document.getElementById("formMessage");

    form.addEventListener("submit", event => {
      event.preventDefault();

      formMessage.textContent =
        "Thanks! Your inquiry has been received. We'll be in touch shortly.";
      formMessage.classList.remove("hidden");

      form.reset();
    });
  </script>

</body>
</html>
