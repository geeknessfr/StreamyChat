# Contributing

**The only thing open here is translation.** The source code is private, so there is nothing to
pull-request into it — but the wording of the application is entirely in your hands.

*[En français, plus bas](#contribuer)*

## What you are translating

StreamyChat's interface lives in [gettext](https://www.gnu.org/software/gettext/) catalogues:

| File | What it is |
|---|---|
| `lang/messages.pot` | **The template.** Every sentence in the application, in English, untranslated. Start here for a new language. |
| `lang/fr.po` | French. A finished catalogue, if you want to see what one looks like. |

## Adding a language

1. **Install [Poedit](https://poedit.net).** Free, cross-platform, and it does exactly this.
2. **Open `lang/messages.pot`**, and pick your language when it asks.
3. **Translate.** Poedit shows the original sentence and a field for yours.
4. **Save as `<code>.po`** — `de.po`, `es.po`, `pt_BR.po`. Use the code Poedit suggests.
5. **Send it.** A pull request, or attached to an
   [issue](https://github.com/geeknessfr/StreamyChat/issues). Both work.

### Try it before you send it

Drop your `.po` into the `lang` folder of your data directory, then restart StreamyChat and pick
your language under **Settings → Advanced → Language**.

| Install type | Where the folder is |
|---|---|
| Installed | `%APPDATA%\StreamyChat\lang` |
| Portable | `StreamyChat-data\lang`, next to the executable |

## Things worth knowing

**A `%s` or a `%d` is a hole, not a word.** It is replaced at runtime by a name, a number or a
duration. Keep every one of them, and put them where your language needs them — the order can
change, and that is fine.

**Some sentences have a singular and a plural form.** Poedit shows one field per form, and it
knows how many your language needs — Polish gets three, Japanese gets one.

**Some strings are deliberately not translated**, and you will not find them in the template:
the names of the built-in themes, and the language names in the language picker. Both identify
something rather than describe it. A theme name travels inside the file you export, so it has to
read the same for whoever receives it; and someone who picked the wrong language must be able to
recognise their own in a list they can no longer read.

**An unfinished catalogue is fine.** Anything you leave empty falls back to English. Send what
you have.

**Twitch words stay Twitch words.** `ban`, `timeout`, `raid`, `sub`, `clip` — if your language's
streamers say the English word, use the English word. If they have their own, use theirs. The
test is whether you would hear it in a live stream in your language.

---

# Contribuer

**La seule chose ouverte ici, c'est la traduction.** Le code est privé, donc il n'y a rien à
proposer dedans — mais tous les textes de l'application dépendent de toi.

## Ce que tu traduis

Les textes vivent dans des catalogues [gettext](https://www.gnu.org/software/gettext/) :

| Fichier | Ce que c'est |
|---|---|
| `lang/messages.pot` | **Le gabarit.** Toutes les phrases de l'application, en anglais, non traduites. C'est le point de départ. |
| `lang/fr.po` | Le français. Un catalogue terminé, si tu veux voir à quoi ça ressemble. |

## Ajouter une langue

1. **Installe [Poedit](https://poedit.net).** Gratuit, et il fait exactement ça.
2. **Ouvre `lang/messages.pot`**, et choisis ta langue quand il te la demande.
3. **Traduis.** Poedit montre la phrase d'origine et un champ pour la tienne.
4. **Enregistre en `<code>.po`** — `de.po`, `es.po`, `pt_BR.po`. Le code que Poedit propose est
   le bon.
5. **Envoie-le.** En pull request, ou en pièce jointe d'une
   [issue](https://github.com/geeknessfr/StreamyChat/issues). Les deux marchent.

### L'essayer avant de l'envoyer

Dépose ton `.po` dans le dossier `lang` de tes données, relance StreamyChat, et choisis ta langue
dans **Réglages → Avancé → Langue**.

| Type d'installation | Où est le dossier |
|---|---|
| Installée | `%APPDATA%\StreamyChat\lang` |
| Portable | `StreamyChat-data\lang`, à côté de l'exécutable |

## Ce qu'il faut savoir

**Un `%s` ou un `%d` est un trou, pas un mot.** Il est remplacé à l'exécution par un pseudo, un
nombre ou une durée. Garde-les tous, et mets-les là où ta langue les veut — l'ordre peut changer,
c'est prévu.

**Certaines phrases ont un singulier et un pluriel.** Poedit affiche un champ par forme, et il
sait combien ta langue en demande — trois pour le polonais, une pour le japonais.

**Certains textes ne se traduisent pas exprès**, et tu ne les trouveras pas dans le gabarit : les
noms des thèmes fournis, et les noms de langue du sélecteur. Les deux **identifient** au lieu de
décrire. Un nom de thème voyage dans le fichier que tu exportes, donc il doit se lire pareil chez
celui qui le reçoit ; et quelqu'un qui s'est trompé de langue doit reconnaître la sienne dans une
liste qu'il ne sait plus lire.

**Un catalogue incomplet, ce n'est pas grave.** Ce que tu laisses vide retombe sur l'anglais.
Envoie ce que tu as.

**Les mots de Twitch restent les mots de Twitch.** `ban`, `timeout`, `raid`, `sub`, `clip` — si
les streamers de ta langue disent le mot anglais, garde le mot anglais. S'ils ont le leur,
prends le leur. Le test : est-ce que tu l'entendrais dans un live dans ta langue ?
