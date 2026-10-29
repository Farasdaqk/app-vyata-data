VYATA ON — PAKET DEPLOY VERCEL (ROOT)

File utama:
- index.html: aplikasi web VYATA ON
- vercel.json: konfigurasi Vercel
- VYATA-ON-SUPABASE-RLS.sql: SQL pengamanan Supabase (jalankan terpisah di SQL Editor)

CARA DEPLOY DARI HP ANDROID:
1. Ekstrak ZIP ini di HP.
2. Buat REPOSITORY GITHUB BARU khusus VYATA ON (jangan gunakan repo SIPANDU).
3. Upload ISI folder ini ke root repository. Pastikan index.html dan vercel.json terlihat langsung di halaman utama repo, bukan berada di dalam subfolder.
4. Di Vercel, Add New → Project, impor repository baru tersebut.
5. Framework Preset: Other. Root Directory: ./ (root repo). Build Command kosong/tidak digunakan. Output Directory: ./ (atau default static output).
6. Deploy. Setelah selesai, buka domain .vercel.app yang dihasilkan.
7. Jika sebelumnya deployment menghasilkan 404, buka Project → Deployments → Redeploy setelah memastikan index.html berada di root.

PENTING:
- Jangan mengubah proyek SIPANDU atau domain rindamsiliwangi.tech.
- Jangan unggah service_role/secret key ke HTML atau GitHub.
- Paket ini adalah web build; APK lama tidak otomatis ikut berubah.
- Jalankan SQL pengamanan setelah memastikan isi SQL sesuai proyek dan cadangkan data penting terlebih dahulu.
- Integrasi belum dianggap lulus sampai login dan sinkronisasi diuji langsung.
