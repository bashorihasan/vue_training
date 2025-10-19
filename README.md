<<<<<<< HEAD
# vue_training
=======
# TechVision - Company Profile Website

Website Company Profile profesional yang dibuat dengan Vue.js, menggunakan **pnpm** dan **Vite**.

## 📋 Deskripsi

Project ini adalah website Company Profile modern yang dibuat untuk mendemonstrasikan kemampuan Vue.js dalam membangun website profesional. Website ini menggunakan Vue 3 dengan build tool Vite dan package manager pnpm, menampilkan berbagai section yang umum ditemukan pada website perusahaan.

## ✨ Fitur & Sections

1. **Navigation Bar** - Navbar responsif dengan smooth scrolling dan mobile menu
2. **Hero Section** - Landing section dengan gradient background dan call-to-action buttons
3. **About Us** - Informasi perusahaan dengan statistik dan visual menarik
4. **Services** - Grid of services dengan icon dan deskripsi (6 layanan)
5. **Team** - Profil tim dengan card layout dan social media links
6. **Contact Form** - Form kontak dengan validasi dan informasi kontak
7. **Footer** - Footer lengkap dengan links, social media, dan newsletter subscription

## 🚀 Cara Menjalankan

### Prerequisites
- Node.js (v18 atau lebih baru)
- pnpm (install dengan `npm install -g pnpm`)

### Installation & Running

```bash
# Install dependencies
pnpm install

# Run development server
pnpm dev

# Build for production
pnpm build

# Preview production build
pnpm preview
```
## 📚 Konsep Vue.js yang Dipelajari

- **Single File Components (SFC)** - Komponen Vue dalam satu file (.vue)
- **Component Architecture** - Membagi aplikasi menjadi 7 komponen berbeda
- **Data Binding** - Mengikat data ke template ({{ }})
- **Event Handling** - @click, @submit, @mouseenter, @mouseleave
- **v-model** - Two-way data binding untuk form input
- **v-for** - Rendering list/array untuk services, team, social links
- **v-if/v-show** - Conditional rendering untuk mobile menu dan success message
- **v-html** - Rendering HTML dinamis untuk icons
- **Methods** - Fungsi untuk handle form, scroll, toggle menu
- **Lifecycle Hooks** - mounted() dan beforeUnmount()
- **Scoped Styles** - CSS yang hanya berlaku untuk komponen tertentu
- **CSS Animations** - Keyframe animations dan transitions
- **Responsive Design** - Mobile-first approach dengan media queries
- **Lifecycle Hooks** - Menggunakan mounted() hook
- **Props & Component Communication** - Komunikasi antar komponen
- **Scoped Styles** - CSS yang hanya berlaku untuk komponen tertentu

## 🛠️ Teknologi yang Digunakan

- **Vue.js 3** - Progressive JavaScript Framework
- **Vite** - Next Generation Frontend Tooling
- **pnpm** - Fast, disk space efficient package manager
- **HTML5** - Markup language
- **CSS3** - Styling dengan modern features
## 📁 Struktur Project

```
vue_training/
├── public/              # Static assets
├── src/
│   ├── components/      # Vue components
│   │   ├── Navbar.vue      # Navigation bar dengan mobile menu
│   │   ├── Hero.vue        # Hero/landing section
│   │   ├── About.vue       # About us section
│   │   ├── Services.vue    # Services grid
│   │   ├── Team.vue        # Team members cards
│   │   ├── Contact.vue     # Contact form & info
│   │   └── Footer.vue      # Footer dengan links & newsletter
│   ├── App.vue         # Root component
│   └── main.js         # Application entry point
├── index.html          # HTML template
├── vite.config.js      # Vite configuration
├── package.json        # Dependencies & scripts
## 🎨 Fitur Design

- **Fully Responsive** - Optimal di semua device (desktop, tablet, mobile)
- **Gradient Backgrounds** - Modern gradient colors
- **Card-based Layout** - Clean card design untuk services dan team
- **Smooth Animations** - fadeIn, slideIn, hover effects
- **Smooth Scrolling** - Navigation dengan smooth scroll
- **Mobile Menu** - Hamburger menu untuk mobile devices
- **Modern Color Scheme** - Professional color palette
## 🎯 Komponen-Komponen

### Navbar.vue
- Fixed navigation dengan scroll detection
- Mobile hamburger menu dengan animation
- Smooth scroll ke sections

### Hero.vue
- Full-screen landing section
- Gradient background dengan overlay
- Call-to-action buttons
- CSS animations (fadeInUp)

### About.vue
- Company description
- Statistics grid (4 stats)
- Image placeholder dengan gradient
- Responsive two-column layout

### Services.vue
- 6 service cards dengan hover effects
- SVG icons untuk setiap service
- Grid layout yang responsive
- Smooth transitions

### Team.vue
- Team member cards dengan photos
- Social media links
- Hover effects pada cards
## 🚀 Deployment

Untuk deploy website ini, jalankan:

```bash
pnpm build
```

Hasil build akan tersimpan di folder `dist/` dan siap untuk di-deploy ke hosting seperti:
- Netlify
- Vercel
- GitHub Pages
- Firebase Hosting

---

Selamat belajar Vue.js dengan membuat Company Profile Website! 🎉
- Contact information dengan icons
- Form dengan validasi
- Success message setelah submit
- Responsive two-column layout

### Footer.vue
- Company info dan social links
- Quick links navigation
- Newsletter subscription form
- Copyright information

## 📝 Tips Customization

1. **Ganti Nama Perusahaan**: Edit `companyName` di `Navbar.vue` dan `Footer.vue`
2. **Ubah Warna Tema**: Ganti gradient colors di setiap komponen
3. **Tambah Services**: Edit array `services` di `Services.vue`
4. **Update Team**: Edit array `teamMembers` di `Team.vue`
5. **Ganti Icons**: Gunakan SVG icons dari [Heroicons](https://heroicons.com/)
6. **Modifikasi Content**: Edit data() di setiap komponen

## 📝 Tips Belajar

1. Lihat struktur komponen di folder `src/components/`
2. Pelajari cara kerja Single File Components (.vue)
3. Pahami bagaimana props dan events bekerja
4. Eksperimen dengan menambah fitur baru
5. Buka console browser untuk melihat log messages
6. Coba modifikasi styling di setiap komponen

## 🔗 Resources

- [Vue.js Official Documentation](https://vuejs.org/)
- [Vite Documentation](https://vitejs.dev/)
- [pnpm Documentation](https://pnpm.io/)
- [Vue.js Guide](https://vuejs.org/guide/introduction.html)
- [Vue.js Examples](https://vuejs.org/examples/)

## 📄 Scripts Available

```bash
pnpm dev        # Start development server
pnpm build      # Build for production
pnpm preview    # Preview production build
```

## 📄 Lisensi

Project ini dibuat untuk tujuan edukasi dan bebas digunakan.

---

Selamat belajar Vue.js dengan pnpm dan Vite! 🎉
>>>>>>> a55c487 (initial project)
