# Indonesian Social Editor

Skill untuk meninjau naskah bahasa Indonesia di media sosial. Ia memeriksa apakah tulisan punya manfaat yang jelas, terdengar wajar untuk pembacanya, dan tetap setia pada bukti setelah disunting.

Pakai saat meninjau caption, rangkaian post, atau carousel. Beri draf, pembaca yang dituju, dan sumber untuk klaim penting jika ada. Skill membantu menemukan bagian yang perlu dipotong, disusun ulang, atau diverifikasi. Tidak perlu memberi skill akses ke akun, token platform, atau akun penerbitan.

## Pemasangan

Unduh atau clone repo ini, lalu salin folder `skills/indonesian-social-editor` ke direktori skill agen yang kamu pakai. Contoh untuk folder skill bersama Codex di Windows:

```powershell
git clone https://github.com/pakde-spill/indonesian-social-editor.git
$skillRoot = Join-Path $env:USERPROFILE '.agents/skills'
$skillTarget = Join-Path $skillRoot 'indonesian-social-editor'
if (Test-Path -LiteralPath $skillTarget) { throw 'Periksa versi skill yang sudah terpasang.' }
New-Item -ItemType Directory -Force -Path $skillRoot | Out-Null
Copy-Item -LiteralPath './indonesian-social-editor/skills/indonesian-social-editor' -Destination $skillTarget -Recurse
```

Mulai sesi baru jika agen belum melihat folder yang baru disalin. Skill v0.1.0 hanya berisi instruksi Markdown; tidak memerlukan paket atau layanan tambahan.

## Contoh permintaan

> Pakai indonesian-social-editor untuk meninjau draf carousel ini. Pembacanya orang yang baru pindah ke kos. Tandai langkah yang kurang berguna, benahi transisi yang kaku, dan pisahkan klaim yang masih perlu dicek.

Hasil review bisa berupa draf yang lolos sunting, saran revisi isi atau bahasa, atau catatan bagian yang harus ditahan untuk verifikasi. Keputusan akhir tetap di editor.

Lisensi: [MIT](LICENSE).
