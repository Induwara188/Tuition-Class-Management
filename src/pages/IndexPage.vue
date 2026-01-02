<template>
  <q-page class="bg-black text-white">
    <!-- Modern Floating Navbar -->
    <div class="fixed-top q-pa-md flex flex-center" style="z-index: 50; pointer-events: none">
      <div
        class="glass-nav row items-center justify-between q-px-xl q-py-sm"
        style="pointer-events: auto; width: 100%; max-width: 900px; border-radius: 100px"
      >
        <!-- Logo -->
        <div class="row items-center cursor-pointer">
          <q-icon name="school" size="24px" class="q-mr-sm" />
          <div class="text-h6 text-weight-bold tracking-tight">Learnly</div>
        </div>

        <!-- Links (Desktop) -->
        <div class="row q-gutter-x-lg gt-sm relative-position text-grey-4">
          <q-btn flat dense no-caps label="Features" class="nav-link text-subtitle2" />
          <q-btn flat dense no-caps label="How it Works" class="nav-link text-subtitle2" />
          <q-btn flat dense no-caps label="Pricing" class="nav-link text-subtitle2" />
          <q-btn flat dense no-caps label="Contact" class="nav-link text-subtitle2" />
        </div>

        <!-- Mobile Menu Button -->
        <q-btn
          flat
          round
          icon="menu"
          class="lt-md text-white q-ml-sm"
          @click="mobileMenuOpen = true"
        />

        <!-- CTA (Desktop) -->
        <q-btn
          rounded
          unelevated
          color="white"
          text-color="black"
          no-caps
          label="Login"
          class="text-weight-bold q-px-lg hover-glow gt-xs"
        />
      </div>
    </div>

    <!-- Mobile Menu Dialog -->
    <q-dialog v-model="mobileMenuOpen" position="right" maximized>
      <q-card class="mobile-menu-card" style="width: 280px; max-width: 85vw">
        <q-card-section class="row items-center justify-between q-pb-md q-pt-lg">
          <div class="text-h5 text-weight-bold text-white">Menu</div>
          <q-btn icon="close" flat round dense v-close-popup color="white" />
        </q-card-section>

        <q-separator dark />

        <q-card-section class="q-pt-lg q-pb-xl">
          <div class="column q-gutter-y-md">
            <div class="mobile-menu-item text-h6 cursor-pointer" v-close-popup>Features</div>
            <div class="mobile-menu-item text-h6 cursor-pointer" v-close-popup>How it Works</div>
            <div class="mobile-menu-item text-h6 cursor-pointer" v-close-popup>Pricing</div>
            <div class="mobile-menu-item text-h6 cursor-pointer" v-close-popup>Contact</div>
          </div>

          <q-separator dark class="q-my-xl" />

          <q-btn
            rounded
            unelevated
            color="white"
            text-color="black"
            label="Login"
            class="full-width text-weight-bold hover-glow"
            size="md"
          />
        </q-card-section>
      </q-card>
    </q-dialog>

    <!-- Hero Section -->
    <section class="row items-center justify-center relative-position overflow-hidden hero-section">
      <div class="container mx-auto row items-center q-px-md" style="max-width: 1200px; z-index: 1">
        <div class="col-12 col-md-6 q-pr-md-xl text-center text-md-left">
          <div class="text-overline text-grey-5 q-mb-sm tracking-widest">NEXT GEN MANAGEMENT</div>
          <h1 class="hero-title text-weight-bolder q-mt-none q-mb-md leading-tight">
            Elevate Your <br />
            <span style="color: #9e9e9e">Tuition Class</span>
          </h1>
          <p class="hero-description q-mb-lg font-light" style="line-height: 1.6">
            A powerful, monochrome solution to streamline student attendance, payments, and
            performance. Focus on teaching, we handle the rest.
          </p>
          <div class="row q-gutter-sm q-gutter-md-md justify-center justify-md-start hero-buttons">
            <q-btn
              unelevated
              rounded
              color="white"
              text-color="black"
              label="Get Started"
              class="hero-btn q-px-lg q-px-md-xl text-weight-bold hover-glow"
              no-caps
            />
            <q-btn
              outline
              rounded
              color="white"
              label="Watch Demo"
              class="hero-btn q-px-lg q-px-md-xl"
              no-caps
              icon="play_arrow"
            />
          </div>

          <div class="row items-center hero-social justify-center justify-md-start">
            <div class="row -space-x-4">
              <q-avatar
                size="40px"
                class="bg-grey-9 text-white border-2 border-black"
                title="User 1"
                >U1</q-avatar
              >
              <q-avatar
                size="40px"
                class="bg-grey-9 text-white border-2 border-black"
                style="margin-left: -10px"
                title="User 2"
                >U2</q-avatar
              >
              <q-avatar
                size="40px"
                class="bg-grey-9 text-white border-2 border-black"
                style="margin-left: -10px"
                title="User 3"
                >U3</q-avatar
              >
              <div
                class="flex flex-center bg-white text-black rounded-borders q-px-sm text-caption text-weight-bold border-2 border-black"
                style="height: 40px; border-radius: 50%; margin-left: -10px"
              >
                +2k
              </div>
            </div>
            <div class="q-ml-md text-grey-5 text-caption">Trusted by tutors island-wide</div>
          </div>
        </div>

        <div class="col-12 col-md-6 hero-image-col relative-position">
          <!-- Image Container with Glass effect -->
          <div class="glass-card q-pa-sm relative-position" style="border-radius: 24px">
            <q-img
              src="~assets/hero-dashboard.png"
              class="shadow-24"
              style="border: 1px solid #333; border-radius: 20px"
              alt="Dashboard Preview"
            >
              <template v-slot:loading>
                <div class="text-white">Loading...</div>
              </template>
            </q-img>

            <!-- Floating Elements for Depth (Hidden on mobile) -->
            <q-card
              class="absolute bg-black text-white shadow-10 q-pa-sm gt-sm"
              style="bottom: -20px; left: -20px; border: 1px solid #333; width: 180px"
            >
              <div class="row items-center justify-between q-mb-xs">
                <div class="text-caption text-grey">Total Students</div>
                <q-icon name="trending_up" color="green" />
              </div>
              <div class="text-h5 text-weight-bold">1,240</div>
            </q-card>

            <q-card
              class="absolute bg-white text-black shadow-10 q-pa-sm gt-sm"
              style="top: 40px; right: -30px; border: 1px solid #ccc; width: 160px"
            >
              <div class="row items-center q-mb-xs">
                <q-icon name="check_circle" color="black" class="q-mr-xs" />
                <div class="text-caption text-weight-bold">Attendance</div>
              </div>
              <div class="text-caption text-grey-8">Class A - 98%</div>
            </q-card>
          </div>
        </div>
      </div>

      <!-- Scroll Indicator -->
      <div class="absolute-bottom text-center q-pb-lg animate-bounce">
        <q-icon name="keyboard_arrow_down" size="lg" color="grey-6" />
      </div>
    </section>

    <!-- Stats Section -->
    <section class="q-py-xl bg-grey-10 border-top border-grey-9">
      <div class="container mx-auto row justify-center q-gutter-y-lg" style="max-width: 1000px">
        <div class="col-6 col-md-3 text-center">
          <div class="stat-number text-weight-bold">50+</div>
          <div class="text-grey-5 q-mt-sm stat-label">Tution Centers</div>
        </div>
        <div class="col-6 col-md-3 text-center">
          <div class="stat-number text-weight-bold">12k</div>
          <div class="text-grey-5 q-mt-sm stat-label">Students Managed</div>
        </div>
        <div class="col-6 col-md-3 text-center">
          <div class="stat-number text-weight-bold">99.9%</div>
          <div class="text-grey-5 q-mt-sm stat-label">System Uptime</div>
        </div>
        <div class="col-6 col-md-3 text-center">
          <div class="stat-number text-weight-bold">24/7</div>
          <div class="text-grey-5 q-mt-sm stat-label">Support</div>
        </div>
      </div>
    </section>

    <!-- Features Section -->
    <section class="q-py-xl relative-position">
      <div class="container mx-auto q-px-md" style="max-width: 1200px">
        <div class="text-center q-mb-xl">
          <div class="text-overline text-grey-5">POWERFUL TOOLS</div>
          <h2 class="text-h3 text-weight-bold q-mt-sm">Everything you need</h2>
        </div>

        <div class="row q-col-gutter-lg">
          <!-- Feature 1 -->
          <div class="col-12 col-md-4">
            <q-card class="glass-card q-h-full hover-effect" style="border-radius: 24px">
              <q-card-section class="q-pa-lg">
                <div class="bg-white text-black inline-block q-pa-md rounded-borders q-mb-md">
                  <q-icon name="people" size="md" />
                </div>
                <div class="text-h6 text-weight-bold q-mb-sm">Student Management</div>
                <p class="text-grey-5">
                  Effortlessly manage student profiles, enrollments, and history in one secure
                  database.
                </p>
              </q-card-section>
            </q-card>
          </div>

          <!-- Feature 2 -->
          <div class="col-12 col-md-4">
            <q-card class="glass-card q-h-full hover-effect" style="border-radius: 24px">
              <q-card-section class="q-pa-lg">
                <div class="bg-white text-black inline-block q-pa-md rounded-borders q-mb-md">
                  <q-icon name="qr_code_scanner" size="md" />
                </div>
                <div class="text-h6 text-weight-bold q-mb-sm">Smart Attendance</div>
                <p class="text-grey-5">
                  QR code based check-ins and real-time SMS notifications to parents.
                </p>
              </q-card-section>
            </q-card>
          </div>

          <!-- Feature 3 -->
          <div class="col-12 col-md-4">
            <q-card class="glass-card q-h-full hover-effect" style="border-radius: 24px">
              <q-card-section class="q-pa-lg">
                <div class="bg-white text-black inline-block q-pa-md rounded-borders q-mb-md">
                  <q-icon name="payments" size="md" />
                </div>
                <div class="text-h6 text-weight-bold q-mb-sm">Fee Management</div>
                <p class="text-grey-5">
                  Track payments, issue digital receipts, and generate financial reports instantly.
                </p>
              </q-card-section>
            </q-card>
          </div>

          <!-- Feature 4 -->
          <div class="col-12 col-md-4">
            <q-card class="glass-card q-h-full hover-effect" style="border-radius: 24px">
              <q-card-section class="q-pa-lg">
                <div class="bg-white text-black inline-block q-pa-md rounded-borders q-mb-md">
                  <q-icon name="insights" size="md" />
                </div>
                <div class="text-h6 text-weight-bold q-mb-sm">Performance Analytics</div>
                <p class="text-grey-5">
                  Visualize growth and identify trends with powerful built-in analytics dashboard.
                </p>
              </q-card-section>
            </q-card>
          </div>

          <!-- Feature 5 -->
          <div class="col-12 col-md-4">
            <q-card class="glass-card q-h-full hover-effect" style="border-radius: 24px">
              <q-card-section class="q-pa-lg">
                <div class="bg-white text-black inline-block q-pa-md rounded-borders q-mb-md">
                  <q-icon name="schedule" size="md" />
                </div>
                <div class="text-h6 text-weight-bold q-mb-sm">Class Scheduling</div>
                <p class="text-grey-5">
                  Organize timetables and manage hall allocations without conflicts.
                </p>
              </q-card-section>
            </q-card>
          </div>

          <!-- Feature 6 -->
          <div class="col-12 col-md-4">
            <q-card class="glass-card q-h-full hover-effect" style="border-radius: 24px">
              <q-card-section class="q-pa-lg">
                <div class="bg-white text-black inline-block q-pa-md rounded-borders q-mb-md">
                  <q-icon name="shield" size="md" />
                </div>
                <div class="text-h6 text-weight-bold q-mb-sm">Secure Data</div>
                <p class="text-grey-5">
                  Enterprise-grade security to keep specific data safe and accessible only to you.
                </p>
              </q-card-section>
            </q-card>
          </div>
        </div>
      </div>
    </section>

    <!-- Call to Action -->
    <section class="q-py-xl text-center bg-grey-10 text-white">
      <div class="container mx-auto q-px-md" style="max-width: 800px">
        <h2 class="text-h3 text-weight-bold q-mb-md">Ready to Modernize?</h2>
        <p class="text-h6 text-grey-5 q-mb-xl">
          Join hundreds of tutors who have transformed their class management experience.
        </p>
        <q-btn
          unelevated
          rounded
          color="white"
          text-color="black"
          label="Start Free Trial"
          size="lg"
          class="q-px-xl text-weight-bold hover-glow"
          no-caps
        />
      </div>
    </section>

    <!-- Footer -->
    <footer class="bg-black text-grey-5 q-py-xl border-top border-grey-9">
      <div class="container mx-auto q-px-md" style="max-width: 1200px">
        <div class="row q-col-gutter-xl">
          <div class="col-12 col-md-4">
            <div class="row items-center q-mb-md">
              <q-icon name="school" size="24px" class="q-mr-sm text-white" />
              <div class="text-h5 text-white text-weight-bold tracking-tight">Learnly</div>
            </div>
            <p>Empowering educators with advanced technology for seamless class management.</p>
          </div>
          <div class="col-12 col-md-2">
            <div class="text-white text-weight-bold q-mb-md">Product</div>
            <div class="q-gutter-y-sm flex column">
              <a href="#" class="text-grey-5 no-decoration hover:text-white">Features</a>
              <a href="#" class="text-grey-5 no-decoration hover:text-white">Pricing</a>
              <a href="#" class="text-grey-5 no-decoration hover:text-white">Case Studies</a>
            </div>
          </div>
          <div class="col-12 col-md-2">
            <div class="text-white text-weight-bold q-mb-md">Company</div>
            <div class="q-gutter-y-sm flex column">
              <a href="#" class="text-grey-5 no-decoration hover:text-white">About</a>
              <a href="#" class="text-grey-5 no-decoration hover:text-white">Careers</a>
              <a href="#" class="text-grey-5 no-decoration hover:text-white">Contact</a>
            </div>
          </div>
          <div class="col-12 col-md-4">
            <div class="text-white text-weight-bold q-mb-md">Stay Updated</div>
            <div class="glass-input row items-center q-px-md q-py-xs">
              <q-input
                borderless
                dark
                dense
                placeholder="Enter email address"
                class="col"
                input-class="text-white"
              />
              <q-btn
                flat
                rounded
                dense
                no-caps
                label="SUBSCRIBE"
                color="white"
                class="text-weight-bold"
              />
            </div>
          </div>
        </div>
        <div class="q-mt-xl text-center text-caption q-pt-lg border-t border-grey-9">
          &copy; 2024 Tuition Class Management System. All rights reserved.
        </div>
      </div>
    </footer>
  </q-page>
</template>

<script setup>
import { ref } from 'vue'

const mobileMenuOpen = ref(false)
</script>

<style scoped>
.glass-input {
  background: rgba(255, 255, 255, 0.05);
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 50px;
}
/* Glass Nav */
.glass-nav {
  background: rgba(10, 10, 10, 0.7);
  backdrop-filter: blur(12px);
  -webkit-backdrop-filter: blur(12px);
  border: 1px solid rgba(255, 255, 255, 0.08);
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.5);
  transition: all 0.3s ease;
}

/* Mobile Menu */
.mobile-menu-card {
  background: rgba(10, 10, 10, 0.95);
  backdrop-filter: blur(20px);
  -webkit-backdrop-filter: blur(20px);
  border-left: 1px solid rgba(255, 255, 255, 0.1);
}

.mobile-menu-item {
  color: #9e9e9e;
  padding: 12px 16px;
  border-radius: 8px;
  transition: color 0.3s ease;
  position: relative;
}

.mobile-menu-item::after {
  content: '';
  position: absolute;
  width: calc(100% - 32px);
  height: 2px;
  bottom: 8px;
  left: 16px;
  background-color: white;
  transform: scaleX(0);
  transform-origin: bottom right;
  transition: transform 0.3s ease-out;
}

.mobile-menu-item:hover::after,
.mobile-menu-item:active::after {
  transform: scaleX(1);
  transform-origin: bottom left;
}

.mobile-menu-item:hover,
.mobile-menu-item:active {
  color: white;
}

.nav-link {
  transition: color 0.3s ease;
  position: relative;
  color: #9e9e9e;
}
/* Hide default Quasar hover background */
.nav-link:deep(.q-focus-helper) {
  display: none !important;
}
.nav-link::after {
  content: '';
  position: absolute;
  width: 100%;
  height: 2px;
  bottom: 4px; /* Slight offset from bottom edge */
  left: 0;
  background-color: white;
  transform: scaleX(0);
  transform-origin: bottom right;
  transition: transform 0.3s ease-out;
}
.nav-link:hover {
  color: white;
  background: transparent;
}
.nav-link:hover::after {
  transform: scaleX(1);
  transform-origin: bottom left;
}

.hover-glow:hover {
  box-shadow: 0 5px 15px rgba(255, 255, 255, 0.15); /* Softer, more dispersed shadow */
  transform: translateY(-1px) scale(1.02);
}

.border-gray {
  border: 1px solid #333;
}
.hover-effect {
  transition:
    transform 0.3s ease,
    box-shadow 0.3s ease;
}
.hover-effect:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 30px rgba(255, 255, 255, 0.05);
  border-color: #555;
}
.glass-card {
  background: rgba(255, 255, 255, 0.05);
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.1);
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
}
.leading-tight {
  line-height: 1.1;
}

@media (min-width: 1024px) {
  .hero-title {
    font-size: 3.75rem; /* text-h2 */
  }
}
@media (max-width: 1023px) {
  .hero-title {
    font-size: 2.5rem; /* ~text-h4 */
  }
}

/* Hero Section Responsive Padding */
.hero-section {
  min-height: 100vh;
  padding-top: 90px;
  padding-bottom: 40px;
}

@media (max-width: 1023px) {
  .hero-section {
    padding-top: 80px;
    padding-bottom: 30px;
  }
}

@media (max-width: 599px) {
  .hero-section {
    padding-top: 100px;
    padding-bottom: 20px;
  }
}

/* Stats Section Responsive */
.stat-number {
  font-size: 3rem;
}

.stat-label {
  font-size: 0.875rem;
}

@media (max-width: 599px) {
  .stat-number {
    font-size: 2rem;
  }
  .stat-label {
    font-size: 0.75rem;
  }
}

/* Hero Section Mobile Improvements */
.hero-description {
  font-size: 1.25rem;
  color: #9e9e9e;
}

@media (max-width: 599px) {
  .hero-description {
    font-size: 0.95rem;
    line-height: 1.5 !important;
  }
}

.hero-btn {
  font-size: 1rem;
}

@media (max-width: 599px) {
  .hero-btn {
    font-size: 0.875rem;
    padding-top: 8px;
    padding-bottom: 8px;
  }
}

.hero-buttons {
  flex-wrap: wrap;
}

@media (max-width: 599px) {
  .hero-buttons {
    gap: 8px !important;
  }
}

.hero-social {
  margin-top: 3rem;
}

@media (max-width: 599px) {
  .hero-social {
    margin-top: 2rem;
  }
}

.hero-image-col {
  margin-top: 3rem;
}

@media (min-width: 1024px) {
  .hero-image-col {
    margin-top: 0;
  }
}

@media (max-width: 599px) {
  .hero-image-col {
    margin-top: 2rem;
  }
}
</style>
