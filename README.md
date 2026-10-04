# Legal AI Assistant

Aplikasi web lokal untuk membantu analisis perkara dan penyusunan dokumen hukum berbasis Gemini AI.

## Fitur utama

- Analisis perkara manual.
- Upload PDF kronologi/perkara.
- Ekstraksi data klien dari kronologi; KTP hanya sebagai pelengkap.
- Prioritas KUHP dan KUHAP terbaru sesuai instruksi aplikasi.
- Dokumen pidana: Pleidoi/Pembelaan, Eksepsi, Banding.
- Dokumen perdata: Gugatan, Jawaban Tergugat, Replik, Duplik, Kesimpulan.
- Dokumen permohonan: Jawaban Termohon, Duplik Termohon.
- Dokumen umum: Somasi, Surat Kuasa Khusus, Surat Kuasa Umum.
- Format dokumen: A4/F4, margin hukum, Times New Roman, justify, spasi 1,5.
- Surat kuasa diarahkan maksimal 2 halaman dan mengikuti format referensi yang digunakan dalam aplikasi.
- Perbaikan Pleidoi untuk mencegah bagian akhir/petitum terpotong sebelum tanda tangan.
- Data perkara disimpan di localStorage browser.

## Struktur

```text
legal-ai-assistant/
├── index.html
├── main.js
├── style.css
├── README.md
└── .gitignore
```

## Menjalankan

### GitHub Pages
1. Upload semua file ke repository GitHub.
2. Buka **Settings → Pages**.
3. Pilih **Deploy from a branch**.
4. Pilih branch utama dan folder `/ (root)`.
5. Simpan dan buka alamat GitHub Pages yang diberikan GitHub.

### Lokal
Bisa dibuka dengan `index.html`, tetapi beberapa browser dapat membatasi fitur tertentu pada `file://`. Untuk hasil yang lebih stabil gunakan server lokal sederhana, misalnya VS Code Live Server atau Python HTTP server.

```bash
python -m http.server 8000
```

Lalu buka `http://localhost:8000`.

## Gemini API Key

Aplikasi meminta pengguna memasukkan Gemini API Key melalui tombol **Gemini API**. Key disimpan di `localStorage` browser dan pemanggilan API dilakukan langsung dari browser. **Jangan menaruh API key pribadi di source code atau commit ke GitHub.** Untuk aplikasi publik/produksi, gunakan backend/proxy agar API key tidak terekspos.

## Catatan privasi

Data klien dan dokumen perkara dapat mengandung data pribadi/sensitif. Gunakan sesuai kewajiban kerahasiaan profesi dan kebijakan privasi yang berlaku. Jangan mengunggah API key atau dokumen rahasia ke repository GitHub.

## Catatan hukum

Aplikasi ini adalah alat bantu penyusunan dan analisis, bukan pengganti penilaian profesional. Dasar hukum, fakta, tanggal peristiwa, nomor perkara, dan dokumen sumber harus diverifikasi sebelum digunakan dalam proses hukum.
