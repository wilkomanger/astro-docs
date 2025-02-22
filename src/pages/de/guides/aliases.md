---
layout: ~/layouts/MainLayout.astro
title: Import-Aliasnamen
description: Eine Einführung in Aliasnamen in Astro.
---

Ein **Aliasname** (kurz **Alias**) ist eine Möglichkeit, um Abkürzungen für Importpfade zu erstellen.

Aliasnamen können dabei helfen, die Entwicklungserfahrung in Codebasen mit vielen Verzeichnissen oder relativen Importpfaden zu verbessern.

```astro
---
// mein-projekt/src/pages/ueber-uns/firma.astro

import Button from '../../components/controls/Button.astro';
import logoUrl from '../../assets/logo.png?url';
---
```

In diesem Beispiel müsste man bei der Entwicklung die Baumbeziehung zwischen `src/pages/ueber-uns/firma.astro`, `src/components/controls/Button.astro` und `src/assets/logo.png` berücksichtigen, um die richtigen relativen Importpfade definieren zu können. Und falls die Datei `firma.astro` jemals verschoben werden sollte, müssten diese Importpfade ebenfalls aktualisiert werden.

Um diese Situation zu verbessern, kannst du Import-Aliasnamen entweder in der Datei `tsconfig.json` oder `jsconfig.json` hinzufügen.

```json
{
  "compilerOptions": {
    "baseUrl": ".",
    "paths": {
      "@components/*": ["src/components/*"],
      "@assets/*": ["src/assets/*"]
    }
  }
}
```

Mit dieser zentralen Änderung kannst du die Importpfade nun überall in deinem Projekt benutzen:

```astro
---
// mein-projekt/src/pages/ueber-uns/firma.astro

import Button from '@components/Button';
import logoUrl from '@assets/logo.png';
---
```

Die von dir definierten Aliasnamen werden auch automatisch in [VS Code](https://code.visualstudio.com/docs/languages/jsconfig) und andere Editoren integriert.
