# Jezdi s Kočkou

Statický web v Astro + TypeScript. Build vytvoří soubory v `dist/`; není potřeba vlastní server ani databáze.

## Lokální spuštění

Vyžaduje Node.js 22.23.4 nebo novější.

```sh
npm install
npm run dev
```

## Ověření a build

```sh
npm run check
npm run build
```

## Nasazení na Netlify

1. Nahrajte tento projekt do samostatného GitHub repozitáře.
2. V Netlify zvolte **Add new site → Import an existing project** a vyberte repozitář.
3. Použijte build command `npm run build` a publish directory `dist` (je nastaveno také v `netlify.toml`).
4. Po prvním deployi otevřete **Forms** a zapněte detekci formulářů (**Enable form detection**), pokud není zapnutá. Potom spusťte nový deploy, aby Netlify formulář načetlo.
5. Ve **Site configuration → Notifications → Emails and webhooks → Form submission notifications** nastavte e-mailové upozornění na `d.vitekerova@gmail.com`.
6. V **Domain management** přidejte `www.jezdiskockou.cz` a nastavte DNS podle údajů, které Netlify zobrazí. Pro hlavní doménu `jezdiskockou.cz` lze nastavit přesměrování na `www`.

Formulář `kontakt` odesílá Netlify Forms na stránku `/dekujeme/` a obsahuje honeypot proti jednoduchému spamu. Před nasazením domény je potřeba provést zkušební odeslání a ověřit notifikační e-mail. Dostupnost formulářů a limity se řídí aktuálním tarifem Netlify.

## On-line přihláška

Přihláška se načítá přímo ze systému Moje-autoškola ve vloženém okně. Skript poskytovatele upravuje jeho výšku podle obsahu; odkaz nad formulářem umožňuje přihlášku otevřít také samostatně. Údaje z přihlášky se odesílají do Moje-autoškola, nikoli do Netlify Forms. Po nasazení ověřte načtení přihlášky a její odeslání přímo v systému poskytovatele.

Fotografie rukou na volantu je stažena z [Pexels](https://www.pexels.com/photo/woman-hands-holding-steering-wheel-12932833/); hravá fotografie kočky je převzata z původního webu.
