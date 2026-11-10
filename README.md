# portslopio

Live site: https://filthyl.github.io/portslopio/

portslopio is a parody portfolio of the projects I have built. Each project is a card with a blurred preview, a short write-up and a "Request access" button. To get the link you must first pass slopCAPTCHA, a gauntlet of deliberately absurd verification trials. It is a single static page with no build step, no cookies, no analytics and no server.

## Projects

| Project | Live link | Trials |
| --- | --- | --- |
| Filth Manor | https://filthyl.github.io/shelves/ | 7 |
| Indian Hate Index | https://filthyl.github.io/hateindex/ | 8 |
| MechWatch | https://filthyl.github.io/MechWatch/ | 7 |
| Ashen Vow (HackeNSlash2D) | https://filthyl.github.io/HackeNSlash2D/ | 6 |
| Parlour | https://filthyl.github.io/Parlour/ | 5 |
| cards- | https://github.com/FilthyL/cards- (a single LICENSE file) | 9 |
| The next one | https://github.com/FilthyL?tab=repositories | 6 |

New repositories with a working GitHub Pages deployment are added on each update. Repositories without a live site are skipped.

## How it works

**slopCAPTCHA.** Each run starts with an "I'm not a robot" checkbox that fails twice, then always includes one free-text and one multiple-choice wild question plus a random mix of trials: a runaway button, a wrong image grid, hold-to-confirm that slips, a no-paste typing test, scroll-to-accept terms, a loading bar that falls back, a maths question with a wrong answer required, a creeping rating slider, a cookie banner, spot-the-real-button, a distorted text captcha and an accusatory "are you a robot" check. Every trial can be passed. Finishing shows the link and a receipt with the time taken. Clearance lasts until the page is refreshed.

**Slop-o-meter.** A gauge in the corner fills as you scroll, hover, click and complete trials, and changes colour across levels from Slop-curious to Terminal slop. At 100% it overloads, rains spaghetti and vents back to 42%. Tapping it triggers escalating plain-text roasts and a poke counter; there are no emoji reactions.

**Ambient slop.** Pop-up ads, rotating banner ads, banger lines and free slop ideas appear while you browse. The Slop Lab has an idea generator with a "Copy as prompt" button and a banger line dispenser.

## Editing

Everything lives in `index.html`. Projects are in the `PROJECTS` array; questions in `FREE_Q` and `MC_Q`; ads in `ADS`; lines in `BANGERS`; idea parts in `IDEA`; meter roasts in `CRINGE`. Screenshots go in `assets/shots/`. To run locally:

```bash
python3 -m http.server 8000
```

## Deployment

`.github/workflows/pages.yml` deploys the repository root to GitHub Pages on every push to `main`. The Pages source must be set to GitHub Actions under Settings, Pages. The site is published at https://filthyl.github.io/portslopio/.
