# GEOҰБТ — Географияны нөлден меңгер

Статикалық сайт (бір `index.html`), серверсіз жұмыс істейді. Прогресс браузердің localStorage-ында сақталады.

## GitHub Pages-ке орналастыру
1. github.com → **New repository** → атауы, мысалы, `geoubt` (Public).
2. **uploading an existing file** сілтемесін басып, `index.html`, `.nojekyll`, `README.md` файлдарын жүктеңіз → **Commit changes**.
3. **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: main / (root) → Save**.
4. 1–2 минуттан кейін сайт `https://<аты>.github.io/geoubt/` мекенжайында ашылады.

## GeoAI (AI-көмекші)
GitHub Pages — тек статикалық хостинг, ал API кілтін сайт кодына қоюға болмайды. Қосу үшін:
1. Cloudflare Workers (немесе Vercel/Netlify function) ішінде прокси жасаңыз: ол `{prompt}` қабылдап, Anthropic API-ға өз құпия кілтімен сұрау жіберіп, `{text}` қайтарады.
2. `index.html` ішіндегі `const AI_URL="";` жолына прокси мекенжайын жазыңыз.
Кілт орнатылмаса, GeoAI «қосылмаған» деп ашық айтады.

## Мазмұнды кеңейту
`index.html` ішінде: `LS` – сабақтар, `QB` – сұрақтар, `G` – бағдарлама, `BK` – оқулықтар, `MP` – карта деректері.
Карталар схемалық. Дәл шекара үшін Natural Earth GeoJSON-ды (қоғамдық домен) `MP.poly` форматына түрлендіріп ауыстыруға болады.
