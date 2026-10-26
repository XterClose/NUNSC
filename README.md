# CODEX Storm Launcher — Base Source v0.1.0

Proyek Android native Kotlin untuk launcher yang berfokus pada Naruto x Boruto: Ultimate Ninja Storm Connections (file game Windows `.exe`).

## Fitur UI dan penyimpanan preferensi
- Pilih folder game memakai Android Storage Access Framework.
- Izin folder disimpan secara persisten.
- Pemeriksaan dasar file `.exe` pada folder terpilih.
- Menu Optimasi FPS: preset Stabil/Seimbang/Visual, target FPS, resolusi, skala resolusi, opsi V-Sync, FSR, shader cache, tekstur, bayangan, dan mode hemat panas.
- Menu grafik dan backend driver.
- Pratinjau layout kontrol gaya PS5 dan opsi overlay.
- Preferensi disimpan dengan SharedPreferences.

## Batasan yang harus diketahui
Ini adalah **source project**, bukan APK terkompilasi. Tombol dan pengaturan FPS menyimpan preferensi di launcher; belum mengubah kinerja game EXE secara langsung. Android tidak dapat menjalankan executable Windows hanya dengan memilih folder. Agar game dapat diluncurkan, proyek perlu diintegrasikan dengan runtime kompatibilitas/emulasi Windows yang sesuai dan legal, kemudian pengaturan grafik, input, dan peluncuran harus dihubungkan ke API runtime tersebut. Jangan menganggap pilihan Vulkan/FSR/shader cache berfungsi kecuali runtime mendukung dan menerapkannya.

## Build
1. Buka folder proyek di Android Studio.
2. Pasang Android SDK Platform 35.
3. Sinkronkan Gradle.
4. Build > Build APK(s).
5. APK debug biasanya ada di `app/build/outputs/apk/debug/app-debug.apk`.

Min SDK 26 (Android 8.0+). Launcher UI dirancang ringan, tetapi performa game PC tetap bergantung pada runtime, GPU, RAM, driver, dan kompatibilitas game.
