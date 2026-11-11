# gitxazina-render

GitXazina agentining video render'i shu repo'ning GitHub Actions workflow'ida bajariladi.
Repo **ommaviy (public)** — ommaviy repolarda GitHub-hosted runner daqiqalari bepul va cheksiz,
shaxsiy repolardagi oylik 2000 daqiqa limiti bunga ta'sir qilmaydi.

Bitta sir bor — `RENDER_SECRET` (Settings → Secrets and variables → Actions → Secrets; qiymati agentdagi
`npm run cli render-secret`). Workflow kirishlari (havolalar) public logda ochiq ko'rinadi, shuning uchun ular
o'zi hech narsaga ruxsat bermaydi: arxivni olish va MP4'ni qaytarish faqat shu sir bilan (`Authorization` sarlavhasi).
Havolalar faqat `PUBLIC_URL` o'zgaruvchisidagi (https) manzilga tegishli bo'lishi shart.

## Sozlash (bir marta)

1. Repo yaratish (public) va shu papkani push qilish.
2. Settings → Secrets and variables → Actions → **Variables** → `PUBLIC_URL` = `https://gitxazina-agent.onrender.com`
3. Agentning `GITHUB_TOKEN` (fine-grained) ga shu repo uchun **Actions: Read and write** ruxsati (annotatsiya sababi uchun ixtiyoriy **Checks: Read**).
4. Render'da `GITHUB_REPO` = `<egasi>/gitxazina-render`.

Asosiy repo'dagi `.github/workflows/render.yml` o'zgarsa, shu yerga ham nusxalang.
