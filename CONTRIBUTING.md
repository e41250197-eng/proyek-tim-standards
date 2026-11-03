# Contributing Guide

Dokumen ini berisi pedoman standar alur kerja pengembangan perangkat lunak dan penggunaan Git bagi seluruh anggota tim pengembang.

---

## 1. Standar Penamaan Branch (Branching Convention)

Format: `<type>/<short-description>` atau `<type>/<issue-number>-<short-description>`

| Type | Kegunaan | Contoh |
| :--- | :--- | :--- |
| `feature/` | Penambahan fitur baru | `feature/123-user-login` |
| `fix/` | Perbaikan bug non-kritis | `fix/cart-total-calculation` |
| `hotfix/` | Perbaikan darurat langsung di production | `hotfix/payment-gateway-down` |
| `refactor/`| Restrukturisasi kode tanpa mengubah perilaku | `refactor/order-service` |
| `docs/` | Pembaruan atau penambahan dokumentasi | `docs/api-reference` |
| `test/` | Penambahan atau perbaikan unit/integration test | `test/checkout-flow` |
| `chore/` | Pemeliharaan rutin / update dependencies | `chore/update-dependencies` |

### Aturan Penulisan Branch:
- Gunakan huruf kecil semua (lowercase).
- Gunakan tanda hubung (`-`) sebagai pemisah kata, bukan spasi atau garis bawah (`_`).
- Deskripsi singkat, padat, dan jelas (maksimal 50 karakter).
- Cantumkan nomor tiket/isu jika ada.

---

## 2. Standar Commit Message (Conventional Commits)

Format:
```text
<type>(<scope>): <subject>

[body opsional]

[footer opsional]

### Aturan Penulisan Commit:
- **Subject**: Wajib huruf kecil (lowercase), diawali kata kerja imperatif (contoh: `add`, `fix`), tanpa titik di akhir.
- Maksimal 50 karakter untuk subject.
- Pisahkan subject dan body dengan 1 baris kosong.
- Referensikan isu bila ada: `Closes #123`.

---

## 3. Standar Pull Request (PR)

- Judul PR mengikuti format commit: `<type>(<scope>): <subject>`.
- Ukuran PR ringkas (< 400 baris).
- Wajib minimal 1 approval reviewer & lulus automated check/CI.
- Merge menggunakan **Squash and Merge**.

### Template Deskripsi PR:
```markdown
## Deskripsi
Jelaskan ringkasan perubahan yang dilakukan.

## Perubahan
- [x] Daftar file / fungsionalitas yang diubah

## Tipe Perubahan
- [ ] Bug fix
- [x] Fitur baru
- [ ] Breaking change

## Checklist
- [x] Automated test lulus
- [x] Sudah self-review
- [x] Bebas konflik

## Referensi
Closes #123