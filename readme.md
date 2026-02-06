# 🚀 CHALLENGE: Horizontal Scroll Animation

## 📋 Deskripsi
Challenge untuk membuat animasi scroll horizontal menggunakan CSS Scroll-Driven Animations modern!

## 🎯 Tugas

### 1. Text Overlay Animation (Slide dari Kiri)
Tambahkan text overlay (judul + deskripsi) pada setiap gambar di dalam `.pin-wrap` yang muncul dari **kiri** (slide in) dengan animasi smooth saat di-scroll.

**Requirements:**
- Text overlay menempati 1/4 bagian kanan gambar
- Text harus readable (gunakan gradient background)
- Animasi smooth dengan opacity + transform
- Setiap gambar punya timing animasi berbeda

### 2. End Section Car Animation (Slide dari Kanan)
Tambahkan animasi slide in dari **kanan** untuk gambar mobil di section `.end`.

## 💡 CLUE

### Untuk animasi di dalam horizontal scroll (`.pin-wrap`):
```css
/* Karena scroll tidak secara vertikal, gunakan animation-timeline dari PARENT */
animation-timeline: --section-pin-tl;

/* Atur animation-range yang berbeda untuk setiap elemen */
/* Contoh: */
.image-wrapper:nth-child(2) .image-text {
  animation-range: contain 10% contain 35%;
}
```

### Untuk animasi di section `.end`:
```css
/* Element scroll secara vertikal normal, gunakan view() */
animation-timeline: view();

/* Gunakan animation-range untuk kontrol kapan animasi mulai dan selesai */
animation-range: entry 0% cover 100%;
```

## 🔑 HINT
- ⚠️ Perhatikan perbedaan cara kerja `view()` vs custom timeline
- 🎨 Element di dalam horizontal scroll butuh pendekatan berbeda!
- 📐 Text overlay: `position: absolute` dengan `width: 25%`
- 🎭 Gradient background: `linear-gradient(to right, rgba(0, 0, 0, 0.85), transparent)`

## ✅ BERHASIL?
Bikin screenshot/video demonya, tag: 
- **@ahmdrydn** 
- **@ittstangsel**

---

## 📚 Resources
- [MDN: CSS Scroll-driven Animations](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_scroll-driven_animations)
- [Chrome Developers: Scroll-driven Animations](https://developer.chrome.com/articles/scroll-driven-animations/)


---

**Good luck! Happy coding! 🎉**