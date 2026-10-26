# gitxazina-render

GitXazina agentining video render'i shu repo'ning GitHub Actions workflow'ida bajariladi.
Repo **ommaviy (public)** — ommaviy repolarda GitHub-hosted runner daqiqalari bepul va cheksiz,
shaxsiy repolardagi oylik 2000 daqiqa limiti bunga ta'sir qilmaydi.

Hech qanday sir yo'q: agent loyiha arxivini imzolangan, 2 soatlik havola bilan beradi,
workflow MP4'ni imzolangan havolaga qaytaradi. Havolalar faqat `PUBLIC_URL` o'zgaruvchisidagi manzilga tegishli bo'lishi shart.

## Sozlash (bir marta)

1. Repo yaratish (public) va shu papkani push qilish.
2. Settings → Secrets and variables → Actions → **Variables** → `PUBLIC_URL` = `https://gitxazina-agent.onrender.com`
3. Agentning `GITHUB_TOKEN` (fine-grained) ga shu repo uchun **Actions: Read and write** ruxsati (annotatsiya sababi uchun ixtiyoriy **Checks: Read**).
4. Render'da `GITHUB_REPO` = `<egasi>/gitxazina-render`.

Asosiy repo'dagi `.github/workflows/render.yml` o'zgarsa, shu yerga ham nusxalang.
