# FitByYou

Din personliga träningsapp — genererade träningsprogram med övningsbilder, workout-logger och vilotimer.

## Deploy

Appen är en statisk site — ingen build, inget backend.

### GitHub Pages
1. Pusha hela mappen till ett repo
2. Settings → Pages → Source: `main` branch, `/ (root)`
3. Klart — live på `username.github.io/fitbyyou`

### Lokal
```
npx serve .
```

## Struktur

```
index.html          ← Hela appen (React via CDN + Babel)
manifest.json       ← PWA-manifest
.nojekyll           ← Behövs för GitHub Pages
img/
  female_barbell_hip_thrusts.png
  female_barbell_squats.png
  female_barbell_leg_press.png
  female_wide_grip_lat_pulldowns_back.png
  female_machine_chest_press.png
  female_dumbbell_side_raises.png
```

## Övningsbilder

6 av ~35 övningar har bilder just nu. Övningar utan bild visar gradient-placeholder med emoji.

Bildformat: `img/{gender}_{exercise_name}.png`

## Features

- **3 lägen**: PT-vy, Klient-vy, Solo-träning
- **Solo onboarding**: Namn, kön, mål, nivå, dagar → genererat 2-veckors program
- **Workout logger**: En övning i taget, rep-timer, vilotimer, set-loggning
- **Övningspopup**: Tryck på övningsnamnet → bild + beskrivning + tips
- **Kost-tab**: Måltidsplanering, makrologg, inköpslista
- **Vikt-tab**: Viktlogg med graf
- **Check-in**: Självbedömning
