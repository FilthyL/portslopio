# portslopio

A parody portfolio for the slop I've made. Every project gets a card with a blurred preview, a write-up and a **Request access** button. Then you have to fight your way through **slopCAPTCHA™** before you get the link.

## The slop

| Project | Link | Trials |
| --- | --- | --- |
| Filth Manor | https://filthyl.github.io/shelves/ | 7 |
| Indian Hate Index | https://filthyl.github.io/hateindex/ | 8 |
| KármánNet | https://github.com/FilthyL/karmannet | 7 |
| cards- | https://github.com/FilthyL/cards- (it's just a LICENSE) | 9 |
| portslopio | this page | 5 |
| The next one | https://github.com/FilthyL?tab=repositories | 6 |

## The gauntlet

Each run opens with the "I'm not a robot" checkbox, which fails you twice. After that you always get one free-text wild question and one multiple-choice wild question, plus a random set of these:

- a Continue button that runs away from you
- an image grid that is wrong about everything ("select all squares with slop")
- hold-to-confirm, which "slips" at 94%
- typing a phrase with paste disabled
- Terms of Slop you have to scroll to the bottom of
- a vibe-check loading bar that reaches 99% and drops back to 37%, with a "go faster" button that slows it down
- a maths question where you then have to enter the wrong answer
- a rating slider that creeps back up to 10/10
- a cookie banner where every toggle is load-bearing
- spot the real Continue among decoys like `C0ntinue` and `Contiune`
- "blink twice if you're being held here"
- a distorted text captcha that rejects your first correct answer
- "are you a robot?", where saying no gets you accused

On trial 4 it adds an extra trial on purpose. The progress bar sometimes goes backwards. Once you're through you get the link and a receipt showing how long it took. Clearance lasts until you refresh.

Every trial can be passed. Nothing gets stored or sent anywhere: no cookies, no analytics, no server.

## Editing

It's all in `index.html`. Projects are in the `PROJECTS` array, and the questions are in `FREE_Q` and `MC_Q`. Screenshots go in `assets/shots/`. To run it locally:

```bash
python3 -m http.server 8000
```

## Deploying

`.github/workflows/pages.yml` deploys the repo root to GitHub Pages on every push to `main`. Turn it on under **Settings → Pages → Source: GitHub Actions**. The site will be at https://filthyl.github.io/portslopio/.
